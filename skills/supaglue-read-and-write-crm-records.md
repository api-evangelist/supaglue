---
name: Read and write CRM records through the unified API
description: >-
  Page through a connected customer's accounts, contacts, leads and opportunities, then create or
  update records — one contract regardless of whether the customer is on Salesforce, HubSpot or
  Pipedrive.
api: openapi/_original/supaglue-crm-api-openapi.yml
operations: [listContacts, getContact, createContact, updateContact, upsertContact, searchContacts, listAccounts, upsertAccount, listOpportunities, updateOpportunity, listLeads, upsertLead]
status: historical
---

# Read and write CRM records through the unified API

**Read this first.** Supaglue is retired (repository archived 2024-03-10; `api.supaglue.io` does not
resolve). These steps describe the v0.25.7 contract and apply to a self-hosted deployment.
Base URL: `https://api.supaglue.io/crm/v2`.

## Every request carries three headers

```
x-api-key: <application key>
x-customer-id: <your id for the customer>
x-provider-name: salesforce | hubspot | pipedrive | ms_dynamics_365_sales | zoho | ...
```

The last two are declared `required` at the path level of every unified operation. Omit them and the
call has no credential to use — there is no default provider.

## Reading

1. `listContacts` — `GET /contacts`. Page with `cursor` and `page_size` (max 1000). The body is
   always `{"pagination":{"next","previous","total_count"},"records":[...]}`; follow
   `pagination.next` until it is null.
2. For an incremental pull, add `modified_after` (ISO 8601, URI-encoded). This is the field a
   warehouse sync should key on.
3. Decide where the data comes from before you call:
   - `read_from_cache=true` reads Supaglue's Managed Destination cache — fast, but only valid if the
     object is actually synced there.
   - default reads the provider live and counts against **their** rate limit, not Supaglue's.
   - `include_raw_data=true` returns the untouched provider payload beside the unified fields; use it
     whenever the unified model loses something you need.
4. `getContact` — `GET /contacts/{contact_id}` for a single record.
   `searchContacts` — `POST /contacts/_search` to look one up by a filterable field (email, phone)
   instead of scanning.

## Writing

5. `createContact` — `POST /contacts` creates unconditionally. There is **no** `Idempotency-Key`
   header in this API, so a retried create makes a duplicate.
6. Prefer `upsertContact` — `POST /contacts/_upsert`, which takes an `upsert_on` field (e.g. email)
   and is the only safe-to-retry write. The same shape exists as `upsertAccount`, `upsertLead` and
   `upsertAssociation`.
7. `updateContact` — `PATCH /contacts/{contact_id}` for partial updates. The same pattern covers
   `updateAccount`, `updateLead`, `updateOpportunity`.

## Failure handling

- `429 TOO_MANY_REQUESTS_ERROR` — back off. No `X-RateLimit-*` or `Retry-After` headers are
  documented; you are flying blind, so use exponential backoff.
  `getConnectionRateLimitInfo` in the Management API reports the **provider's** remaining quota.
- `499 REMOTE_PROVIDER_ERROR` — the SaaS rejected it. Read `errors[0].detail`; that text is theirs.
- `500 CACHE_INVALIDATION_ERROR` — the write reached the provider but Supaglue could not refresh the
  copy in your Destination. Do not replay the write; re-sync instead.
- Anything the unified model cannot express: `sendPassthroughRequest` —
  `POST https://api.supaglue.io/actions/v2/passthrough` calls the native provider API with the same
  managed credentials.
