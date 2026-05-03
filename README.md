# Supaglue

Supaglue is an open-source unified API platform that enables B2B SaaS developers to build product integrations with CRM, HRIS, sales engagement, ticketing, and other business applications. It provides a unified API layer that abstracts away provider-specific differences, managed OAuth authentication, and data syncing to data warehouses.

Supported providers include Salesforce, HubSpot, Pipedrive, Zendesk, Outreach, Salesloft, and 15+ others. Available as managed cloud service (api.supaglue.io) and self-hosted open-source.

**URL:** [APIs.yml](https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/apis.yml)

## Tags

CRM, HRIS, Unified API, Open Source, Integrations, Sales Engagement

## APIs

### Supaglue Management API
Configure customers, connections, sync configs, data destinations (BigQuery, Snowflake, Redshift, Postgres), schemas, entity mappings, and sync operations. Auth: x-api-key header. Base: `https://api.supaglue.io/mgmt/v2`. 50 operations.

**URL:** [https://docs.supaglue.com/api/v2/mgmt/management-api](https://docs.supaglue.com/api/v2/mgmt/management-api)

**Tags:** Management, Customers, Connections, Sync, Destinations

**Properties:**
- [Documentation](https://docs.supaglue.com/api/v2/mgmt/management-api)
- [OpenAPI](openapi/supaglue-management-api-openapi.yml)

### Supaglue Unified CRM API
Single interface for CRM data (accounts, contacts, leads, opportunities, custom objects) across Salesforce, HubSpot, Pipedrive and more. Auth: x-api-key + x-customer-id + x-provider-name headers. Base: `https://api.supaglue.io/crm/v2`. 47 operations.

**URL:** [https://docs.supaglue.com/api/v2/crm/unified-crm-api](https://docs.supaglue.com/api/v2/crm/unified-crm-api)

**Tags:** CRM, Contacts, Accounts, Opportunities, Leads, Salesforce, HubSpot

**Properties:**
- [Documentation](https://docs.supaglue.com/api/v2/crm/unified-crm-api)
- [OpenAPI](openapi/supaglue-crm-api-openapi.yml)

### Supaglue Unified Engagement API
Single interface for sales engagement data (accounts, contacts, sequences, sequence states, mailboxes) across Outreach, Salesloft, Apollo and more. 25 operations.

**URL:** [https://docs.supaglue.com/api/v2/engagement](https://docs.supaglue.com/api/v2/engagement)

**Tags:** Sales Engagement, Outreach, Salesloft, Sequences, Contacts

**Properties:**
- [Documentation](https://docs.supaglue.com/api/v2/engagement)
- [OpenAPI](openapi/supaglue-engagement-api-openapi.yml)

### Supaglue Unified Ticketing API (Preview)
Single interface for ticketing/support data (accounts, collections, tickets, users) across Zendesk, Linear, and others. 23 operations.

**URL:** [https://docs.supaglue.com/api/v2/ticketing](https://docs.supaglue.com/api/v2/ticketing)

**Tags:** Ticketing, Support, Zendesk, Help Desk

**Properties:**
- [Documentation](https://docs.supaglue.com/api/v2/ticketing)
- [OpenAPI](openapi/supaglue-ticketing-api-openapi.yml)

## Artifacts

| Type | File |
|------|------|
| OpenAPI — Management API | [supaglue-management-api-openapi.yml](openapi/supaglue-management-api-openapi.yml) |
| OpenAPI — Unified CRM API | [supaglue-crm-api-openapi.yml](openapi/supaglue-crm-api-openapi.yml) |
| OpenAPI — Unified Engagement API | [supaglue-engagement-api-openapi.yml](openapi/supaglue-engagement-api-openapi.yml) |
| OpenAPI — Unified Ticketing API | [supaglue-ticketing-api-openapi.yml](openapi/supaglue-ticketing-api-openapi.yml) |
| JSON Schema — CRM Contact | [supaglue-contact-schema.json](json-schema/supaglue-contact-schema.json) |
| JSON Structure — CRM | [supaglue-crm-structure.json](json-structure/supaglue-crm-structure.json) |
| JSON-LD Context | [supaglue-context.jsonld](json-ld/supaglue-context.jsonld) |
| Spectral Rules | [supaglue-rules.yml](rules/supaglue-rules.yml) |
| Capabilities — Shared: Management | [capabilities/shared/management-api.yaml](capabilities/shared/management-api.yaml) |
| Capabilities — Shared: CRM | [capabilities/shared/crm-api.yaml](capabilities/shared/crm-api.yaml) |
| Capabilities — CRM Integration | [capabilities/crm-integration.yaml](capabilities/crm-integration.yaml) |
| Vocabulary | [supaglue-vocabulary.yml](vocabulary/supaglue-vocabulary.yml) |
| Example — List Contacts | [supaglue-list-contacts-example.json](examples/supaglue-list-contacts-example.json) |

## Common Properties

- [Website](https://www.supaglue.com/)
- [Documentation](https://docs.supaglue.com/)
- [GitHub Organization](https://github.com/supaglue-labs)
- [Getting Started](https://docs.supaglue.com/getting-started)

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com
