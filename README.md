# Supaglue (supaglue)

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
