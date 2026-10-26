# Supaglue (supaglue)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Supaglue is an open-source unified API platform that enables B2B SaaS developers to build product integrations with CRM, HRIS, sales engagement, ticketing, and other business applications. It provides a unified API layer that abstracts away provider-specific differences, managed OAuth authentication, data syncing to data warehouses (BigQuery, Snowflake, Redshift, Postgres), and a management API for configuring customers, connections, and sync configurations. Supported providers include Salesforce, HubSpot, Pipedrive, Zendesk, Slack, and 15+ others. The platform is available as a managed cloud service (api.supaglue.io) and as a self-hosted open-source deployment. The GitHub organization is github.com/supaglue-labs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- CRM
- HRIS
- Unified API
- Open Source
- Integrations
- Sales Engagement

## Timestamps

- **Created:** 2026-03-27
- **Modified:** 2026-05-19

## APIs

### Supaglue Management API

The Supaglue Management API configures all aspects of the integration platform. Manages customers (the end users of the integrations), their connections to third-party providers, sync configurations, data destinations (BigQuery, Snowflake, Redshift, Postgres), schema and entity mappings, field mappings, providers, sync operations (trigger/pause/resume), sync run history, and magic link generation for OAuth flows. Authentication uses an API key passed via the x-api-key header. Base URL: https://api.supaglue.io/mgmt/v2.

- **Human URL:** [https://docs.supaglue.com/api/v2/mgmt/management-api](https://docs.supaglue.com/api/v2/mgmt/management-api)

#### Tags

- Management
- Customers
- Connections
- Sync
- Destinations

#### Properties

- [Documentation](https://docs.supaglue.com/api/v2/mgmt/management-api)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-management-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/supaglue-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-engagement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-engagement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-ticketing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-ticketing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Supaglue Unified CRM API

The Supaglue Unified CRM API provides a single interface for reading and writing CRM data across Salesforce, HubSpot, Pipedrive, and other providers. Supports accounts, contacts, leads, opportunities, users, custom objects, standard objects, associations, lists, and metadata (custom object schemas, property definitions). All operations use the x-api-key header plus a customer ID context. Base URL: https://api.supaglue.io/crm/v2.

- **Human URL:** [https://docs.supaglue.com/api/v2/crm/unified-crm-api](https://docs.supaglue.com/api/v2/crm/unified-crm-api)

#### Tags

- CRM
- Contacts
- Accounts
- Opportunities
- Leads
- Salesforce
- HubSpot

#### Properties

- [Documentation](https://docs.supaglue.com/api/v2/crm/unified-crm-api)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-crm-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/supaglue-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-engagement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-engagement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-ticketing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-ticketing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Supaglue Unified Engagement API

The Supaglue Unified Engagement API provides a single interface for reading and writing sales engagement data across Outreach, Salesloft, Apollo, and other sales engagement platforms. Supports accounts, contacts, sequences, sequence states, mailboxes, users, and metadata for custom objects and standard objects. Base URL: https://api.supaglue.io/engagement/v2.

- **Human URL:** [https://docs.supaglue.com/api/v2/engagement](https://docs.supaglue.com/api/v2/engagement)

#### Tags

- Sales Engagement
- Outreach
- Salesloft
- Sequences
- Contacts

#### Properties

- [Documentation](https://docs.supaglue.com/api/v2/engagement)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-engagement-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/supaglue-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-engagement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-engagement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-ticketing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-ticketing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Supaglue Unified Ticketing API

The Supaglue Unified Ticketing API (Preview) provides a single interface for reading ticketing and support data across Zendesk, Linear, and other ticketing platforms. Supports accounts, collections, tickets, tags, contacts, users, and attachments. Base URL: https://api.supaglue.io/ticketing/v2.

- **Human URL:** [https://docs.supaglue.com/api/v2/ticketing](https://docs.supaglue.com/api/v2/ticketing)

#### Tags

- Ticketing
- Support
- Zendesk
- Help Desk

#### Properties

- [Documentation](https://docs.supaglue.com/api/v2/ticketing)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-ticketing-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/supaglue-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-engagement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-engagement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/supaglue-ticketing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/supaglue-ticketing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/supaglue)
- [Website](https://www.supaglue.com/)
- [Documentation](https://docs.supaglue.com/)
- [GitHub Organization](https://github.com/supaglue-labs)
- [Getting Started](https://docs.supaglue.com/getting-started)
- [A P I  Introduction](https://docs.supaglue.com/api/introduction)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
