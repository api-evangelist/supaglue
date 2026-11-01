# Supaglue

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

Supaglue was an open-source unified API platform for B2B SaaS product integrations: a single contract for CRM, engagement, ticketing, enrichment and marketing-automation objects projected across 30+ third-party providers (Salesforce, HubSpot, Pipedrive, Outreach, Salesloft, Zendesk, Apollo and more), plus managed OAuth to those providers, managed syncs into the customer's own warehouse (Postgres, BigQuery, Snowflake, Redshift, S3), a passthrough escape hatch to native provider APIs, and a Management API to configure customers, connections, schemas, entities and sync schedules. Nine first-party OpenAPI documents (v2, x-api-key auth) and nine typed webhook events were published. THE SERVICE IS RETIRED: the GitHub repository (github.com/supaglue-labs) was archived by its owner on 2024-03-10, api.supaglue.io and app.supaglue.io no longer resolve, and supaglue.com now redirects to a HugeDomains sale listing. The MIT-licensed code remains self-hostable, and the contract is preserved here as the historical record of a well-shaped unified API.

**Areas:** CRM · HRIS · Unified API · Open Source · Integration · Sales Engagement · Ticketing · Data Synchronization · Marketing Automation · Data Enrichment · Webhook · Archived

## Supaglue on APIs.io

Everything profiled for Supaglue is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/supaglue/](https://apis.io/providers/supaglue/)** — or go straight to one of the APIs or properties below.

### APIs (41)

- [Supaglue Accounts API](https://apis.io/apis/supaglue/supaglue-accounts-api/) — The `Account` Common Object represents a "company" in CRMs.
- [Supaglue Associations API](https://apis.io/apis/supaglue/supaglue-associations-api/) — The Associations API from Supaglue — 1 operation(s) for associations.
- [Supaglue AssociationSchemas API](https://apis.io/apis/supaglue/supaglue-associationschemas-api/) — An `Association Schema` is an object describing an association between two entities.
- [Supaglue Attachments API](https://apis.io/apis/supaglue/supaglue-attachments-api/) — The Attachment object is used to represent an attachment for a ticket.
- [Supaglue Collections API](https://apis.io/apis/supaglue/supaglue-collections-api/) — The Collection object is used to represent collections of tickets. Collections may include other collections as sub collections.
- [Supaglue Comments API](https://apis.io/apis/supaglue/supaglue-comments-api/) — The Comment object is used to represent a comment on a ticket.
- [Supaglue Connections API](https://apis.io/apis/supaglue/supaglue-connections-api/) — A `Connection` represents a Customer's connection to a Provider.
- [Supaglue ConnectionSyncConfigs API](https://apis.io/apis/supaglue/supaglue-connectionsyncconfigs-api/) — A `ConnectionSyncConfig` is a configuration for how to sync a specific Customer's data from a Provider to a Destination on a schedule.
- [Supaglue Contacts API](https://apis.io/apis/supaglue/supaglue-contacts-api/) — The `Contact` Common Object represents a "contact" in CRMs.
- [Supaglue Customers API](https://apis.io/apis/supaglue/supaglue-customers-api/) — A `Customer` represents one of your customers.
- [Supaglue Destinations API](https://apis.io/apis/supaglue/supaglue-destinations-api/) — A `Destination` is a data store where we write data in your infrastructure.
- [Supaglue Entities API](https://apis.io/apis/supaglue/supaglue-entities-api/) — An [`Entity`](https://docs.supaglue.com/platform/entities/overview) allows you to represent your application data models in Supaglue so customers can map…
- [Supaglue EntityMappings API](https://apis.io/apis/supaglue/supaglue-entitymappings-api/) — An [`Entity Mapping`](https://docs.supaglue.com/platform/entities/overview#entity-mapping) maps an…
- [Supaglue Leads API](https://apis.io/apis/supaglue/supaglue-leads-api/) — The `Lead` Common Object represents a "potential customer" in CRMs.
- [Supaglue Lists API](https://apis.io/apis/supaglue/supaglue-lists-api/) — The `List` Object represents a collection of CRM records.
- [Supaglue Magic Links API](https://apis.io/apis/supaglue/supaglue-magic-links-api/) — A `Magic Link` is a secure URL that allows your customers to connect their accounts to Supaglue.
- [Supaglue Mailboxes API](https://apis.io/apis/supaglue/supaglue-mailboxes-api/) — The `Mailbox` Common Object is used to represent email mailbox, used within the application for sending and syncing emails.
- [Supaglue Opportunities API](https://apis.io/apis/supaglue/supaglue-opportunities-api/) — The `Opportunity` Common Object represents a "deal opportunity" in CRMs.
- [Supaglue Properties API](https://apis.io/apis/supaglue/supaglue-properties-api/) — A `Property` is a field in a Provider Object.
- [Supaglue Providers API](https://apis.io/apis/supaglue/supaglue-providers-api/) — A `Provider` is a third-party SaaS tool we can connect to (e.g. Salesforce).
- [Supaglue Schemas API](https://apis.io/apis/supaglue/supaglue-schemas-api/) — A [`Schema`](https://docs.supaglue.com/platform/objects/overview#schemas) allows you to normalize fields for customers across a single Provider object.…
- [Supaglue Sequence States API](https://apis.io/apis/supaglue/supaglue-sequence-states-api/) — The `Sequence State` Common Object represents the state of a contact in a sequence, commonly known as a "sequence membership".
- [Supaglue Sequences API](https://apis.io/apis/supaglue/supaglue-sequences-api/) — The `Sequence` Common Object represents a "sequence" in Engagements.
- [Supaglue StandardObjects API](https://apis.io/apis/supaglue/supaglue-standardobjects-api/) — The StandardObjects API from Supaglue — 2 operation(s) for standardobjects.
- [Supaglue StandardObjectSchemas API](https://apis.io/apis/supaglue/supaglue-standardobjectschemas-api/) — A `Standard Object Schema` is an object schema of a standard object type supported by the provider.
- [Supaglue SyncConfigs API](https://apis.io/apis/supaglue/supaglue-syncconfigs-api/) — A `SyncConfig` is a configuration for how to sync your Customers' data from a Provider to a Destination on a schedule.
- [Supaglue SyncRuns API](https://apis.io/apis/supaglue/supaglue-syncruns-api/) — A `SyncRun` is a single execution of a Sync at a point in time.
- [Supaglue Syncs API](https://apis.io/apis/supaglue/supaglue-syncs-api/) — A `Sync` is a way for a Customer to sync data from a Provider to a Destination on a schedule.
- [Supaglue Tags API](https://apis.io/apis/supaglue/supaglue-tags-api/) — The Tag object is used to represent a tag or label for a ticket.
- [Supaglue Teams API](https://apis.io/apis/supaglue/supaglue-teams-api/) — The Team object is used to represent a team within the company receiving the ticket.
- [Supaglue Tickets API](https://apis.io/apis/supaglue/supaglue-tickets-api/) — The Ticket object is used to represent a ticket or a task within a system.
- [Supaglue Users API](https://apis.io/apis/supaglue/supaglue-users-api/) — The `User` Common Object represents a "user" that can log in to CRMs.
- [Supaglue Forms API](https://apis.io/apis/supaglue/supaglue-forms-api/) — Endpoints for managing and submitting forms
- [Supaglue Hubspot API](https://apis.io/apis/supaglue/supaglue-hubspot-api/) — Hubspot is a CRM Provider.
- [Supaglue Passthrough API](https://apis.io/apis/supaglue/supaglue-passthrough-api/) — Passthrough operations to underlying providers.
- [Supaglue Persons API](https://apis.io/apis/supaglue/supaglue-persons-api/) — Relating to enrichment data that is derived from information about a Person. This may include demographic and firmographic data.
- [Supaglue Salesforce API](https://apis.io/apis/supaglue/supaglue-salesforce-api/) — Salesforce is a CRM Provider.
- [Supaglue Webhook Events API](https://apis.io/apis/supaglue/supaglue-webhook-events-api/) — The Webhook Events API from Supaglue — 0 operation(s) for webhook events.
- [Supaglue Custom Object Schemas API](https://apis.io/apis/supaglue/supaglue-custom-object-schemas-api/) — A `Custom Object Schema` is an object schema defined by the user.
- [Supaglue Custom Objects API](https://apis.io/apis/supaglue/supaglue-custom-objects-api/) — A `Custom Object` is an instance of a `Custom Object Schema`.
- [Supaglue Schema Mappings API](https://apis.io/apis/supaglue/supaglue-schema-mappings-api/) — A `Schema Mapping` is a mapping between a Schema field and fields in your customer's Provider object.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Supaglue Webhooks](https://apis.io/asyncapis/supaglue/supaglue-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [supaglue](https://apis.io/servers/supaglue/supaglue/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Supaglue Agentic Access](https://apis.io/agentic-access/supaglue/supaglue-agentic-access/)

#### JSON Schema (1)

The data models the API reads and writes.

- [Supaglue CRM Contact](https://apis.io/schemas/supaglue/supaglue-contact/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Supaglue Crm Structure](https://apis.io/json-structure/supaglue/supaglue-crm-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Supaglue Context](https://apis.io/jsonld/supaglue/supaglue-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Supaglue Vocabulary](https://apis.io/vocabularies/supaglue/supaglue-vocabulary/)

#### Examples (1)

Example requests and responses.

- [Supaglue List Contacts Example](https://apis.io/examples/supaglue/supaglue-list-contacts-example/)

#### Collections (44)

Postman and Open Collection request collections.

- [Unified CRM Accounts API](https://apis.io/collections/supaglue/open-supaglue-accounts-api/)
- [Actions API](https://apis.io/collections/supaglue/open-supaglue-actions-api/)
- [Unified CRM Accounts Associations API](https://apis.io/collections/supaglue/open-supaglue-associations-api/)
- [Unified CRM Accounts AssociationSchemas API](https://apis.io/collections/supaglue/open-supaglue-associationschemas-api/)
- [Unified CRM Accounts Attachments API](https://apis.io/collections/supaglue/open-supaglue-attachments-api/)
- [Unified CRM Accounts Collections API](https://apis.io/collections/supaglue/open-supaglue-collections-api/)
- [Unified CRM Accounts Comments API](https://apis.io/collections/supaglue/open-supaglue-comments-api/)
- [Unified CRM Accounts Connections API](https://apis.io/collections/supaglue/open-supaglue-connections-api/)
- [Unified CRM Accounts ConnectionSyncConfigs API](https://apis.io/collections/supaglue/open-supaglue-connectionsyncconfigs-api/)
- [Unified CRM Accounts Contacts API](https://apis.io/collections/supaglue/open-supaglue-contacts-api/)
- [Unified CRM API](https://apis.io/collections/supaglue/open-supaglue-crm-api/)
- [Unified CRM Accounts Customers API](https://apis.io/collections/supaglue/open-supaglue-customers-api/)
- [Unified CRM Accounts CustomObjects API](https://apis.io/collections/supaglue/open-supaglue-customobjects-api/)
- [Unified CRM Accounts CustomObjectSchemas API](https://apis.io/collections/supaglue/open-supaglue-customobjectschemas-api/)
- [Data Listing API](https://apis.io/collections/supaglue/open-supaglue-data-api/)
- [Unified CRM Accounts Destinations API](https://apis.io/collections/supaglue/open-supaglue-destinations-api/)
- [Unified Engagement API](https://apis.io/collections/supaglue/open-supaglue-engagement-api/)
- [Unified Enrichment API](https://apis.io/collections/supaglue/open-supaglue-enrichment-api/)
- [Unified CRM Accounts Entities API](https://apis.io/collections/supaglue/open-supaglue-entities-api/)
- [Unified CRM Accounts EntityMappings API](https://apis.io/collections/supaglue/open-supaglue-entitymappings-api/)
- [Unified CRM Accounts Leads API](https://apis.io/collections/supaglue/open-supaglue-leads-api/)
- [Unified CRM Accounts Lists API](https://apis.io/collections/supaglue/open-supaglue-lists-api/)
- [Unified CRM Accounts Magic Links API](https://apis.io/collections/supaglue/open-supaglue-magic-links-api/)
- [Unified CRM Accounts Mailboxes API](https://apis.io/collections/supaglue/open-supaglue-mailboxes-api/)
- [Management API](https://apis.io/collections/supaglue/open-supaglue-management-api/)
- …and 19 more published on APIs.io

#### Overlays (9)

OpenAPI overlays, including conversational phrasing for each operation.

- [Supaglue Actions Overlay](https://apis.io/overlays/supaglue/supaglue-actions-overlay/)
- [Supaglue Crm Overlay](https://apis.io/overlays/supaglue/supaglue-crm-overlay/)
- [Supaglue Data Overlay](https://apis.io/overlays/supaglue/supaglue-data-overlay/)
- [Supaglue Engagement Overlay](https://apis.io/overlays/supaglue/supaglue-engagement-overlay/)
- [Supaglue Enrichment Overlay](https://apis.io/overlays/supaglue/supaglue-enrichment-overlay/)
- [Supaglue Management Overlay](https://apis.io/overlays/supaglue/supaglue-management-overlay/)
- [Supaglue Marketing Automation Overlay](https://apis.io/overlays/supaglue/supaglue-marketing-automation-overlay/)
- [Supaglue Metadata Overlay](https://apis.io/overlays/supaglue/supaglue-metadata-overlay/)
- [Supaglue Ticketing Overlay](https://apis.io/overlays/supaglue/supaglue-ticketing-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Supaglue — jsonschema rules](https://apis.io/rules/supaglue/supaglue-jsonschema-spectral-rules/)
- [Supaglue API Rules](https://apis.io/rules/supaglue/supaglue-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Supaglue Authentication](https://apis.io/security/supaglue/supaglue-authentication/)
- [Supaglue Domain Security](https://apis.io/security/supaglue/supaglue-domain-security/)
- [Supaglue Vulnerability Disclosure](https://apis.io/security/supaglue/supaglue-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Supaglue Plans Pricing](https://apis.io/plans/supaglue/supaglue-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Supaglue Rate Limits](https://apis.io/rate-limits/supaglue/supaglue-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Supaglue Finops](https://apis.io/finops/supaglue/supaglue-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://supaglue.io)
- [Documentation](https://github.com/supaglue-labs/supaglue/tree/main/docs/docs)
- [Getting started](https://github.com/supaglue-labs/supaglue/blob/main/docs/docs/quickstart.mdx)
- [API reference](https://github.com/supaglue-labs/supaglue/tree/main/docs/docs/api/v2)
- [Security](https://github.com/supaglue-labs/supaglue/blob/main/SECURITY.md)
- [Compliance](https://github.com/supaglue-labs/supaglue/blob/main/docs/docs/security_legal/security.md)
- [Terms of service](https://github.com/supaglue-labs/supaglue/blob/main/docs/docs/security_legal/terms.md)
- [Privacy policy](https://github.com/supaglue-labs/supaglue/blob/main/docs/docs/security_legal/privacy.md)
- [GitHub](https://github.com/supaglue-labs)

## API Evangelist rating

**Kin Score 57.0** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 63.3 |
| Contract governance | 31.8 |
| Operational transparency | 42.1 |
| Developer ergonomics | 42.3 |
| Access clarity | 50.0 |

**Agent readiness 32.5** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 43.1** — Employment & Payroll

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/supaglue/](https://apis.io/providers/supaglue/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Supaglue: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/supaglue/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
