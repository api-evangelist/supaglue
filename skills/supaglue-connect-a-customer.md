---
name: Connect a customer to a third-party provider
description: >-
  Register a customer in Supaglue, configure the provider, and get that customer authenticated
  against their SaaS (Salesforce, HubSpot, Outreach, ...) so every later unified call can route to
  their credentials.
api: openapi/_original/supaglue-management-api-openapi.yml
operations: [upsertCustomer, createProvider, getProviders, createMagicLink, getConnections, getConnection, getProviderUserId]
status: historical
---

# Connect a customer to a third-party provider

**Read this first.** Supaglue is retired: the repository was archived 2024-03-10 and
`api.supaglue.io` no longer resolves. These steps are correct against the v0.25.7 contract and run
only against a self-hosted deployment of the MIT-licensed code. Substitute your own base URL for
`https://api.supaglue.io/mgmt/v2`.

## Preconditions

- An application API key, sent as `x-api-key` on every request. There are no scopes; the key is
  application-wide.
- The Management API takes **no** `x-customer-id` / `x-provider-name` headers — those are for the
  unified APIs only.

## Steps

1. **Register the customer.** `upsertCustomer` — `PUT /customers` with your own
   `customer_id` (your application's identifier for them), `name` and `email`. Upsert, so re-running
   this step is safe.
2. **Confirm the provider is configured.** `getProviders` — `GET /providers`. If the provider you
   need is absent, `createProvider` — `POST /providers` with `category` (`crm`, `engagement`,
   `ticketing`, ...), `name` (`salesforce`, `hubspot`, ...), `auth_type` and the OAuth client
   credentials you registered with that SaaS.
3. **Get the customer authenticated.** Either
   - hand them an Embedded Link:
     `https://api.supaglue.io/oauth/connect?applicationId={APPLICATION_ID}&customerId={CUSTOMER_ID}&providerName={PROVIDER_NAME}&returnUrl={RETURN_URL}`
     (URI-encode `returnUrl`; add `loginUrl=https://test.salesforce.com` for a Salesforce sandbox,
     or `scope` for Microsoft Dynamics 365), or
   - `createMagicLink` — `POST /magic_links` to mint a shareable, expiring URL that needs no
     frontend code on your side.
4. **Verify the connection landed.** `getConnections` — `GET /customers/{customer_id}/connections`,
   then `getConnection` — `GET /customers/{customer_id}/connections/{provider_name}`.
   `getProviderUserId` — `GET /customers/{customer_id}/connections/_provider_user_id` confirms which
   remote user the token belongs to.
5. **Listen instead of polling.** The `connection.created` and `connection.deleted` webhooks fire on
   this flow (`asyncapi/supaglue-webhooks.yml`). Payload field `webhook_event_type` carries the type;
   `result` says whether it succeeded. You have 15 seconds to respond, and Svix signs every delivery.

## Rules

- Never retry step 1 or 3 blindly hoping for idempotency: only the `_upsert`-style operations are
  safe to repeat. `upsertCustomer` is; `createProvider` and `createMagicLink` are not.
- Errors come back as `{"errors":[{id, detail, title, code, status, meta}]}`, never
  `application/problem+json`. Quote `errors[0].id` when escalating.
- A `499` is not your bug and not Supaglue's — it is the third-party SaaS rejecting the call, with
  its own message passed through in `detail`.
