---
name: Configure and run a managed sync into your warehouse
description: >-
  Point a Destination at your own Postgres/BigQuery/Snowflake/Redshift/S3, define what to sync on
  what schedule, trigger and pause runs, and watch the results through sync webhooks.
api: openapi/_original/supaglue-management-api-openapi.yml
operations: [createDestination, getDestinations, updateDestination, createSyncConfig, getSyncConfigs, updateSyncConfig, upsertConnectionSyncConfig, getSyncs, triggerSync, pauseSync, resumeSync, getSyncRuns]
status: historical
---

# Configure and run a managed sync into your warehouse

**Read this first.** Supaglue is retired (repository archived 2024-03-10; `api.supaglue.io` does not
resolve). Managed syncs still work in a self-hosted deployment — the sync worker ships in the
archived monorepo. Base URL: `https://api.supaglue.io/mgmt/v2`.

## The chain

`Customer` → `Connection` (to a Provider) → `SyncConfig` (what + how often) → `Sync` (per
connection) → `SyncRun` (one execution). Nothing syncs until all four exist.

## Steps

1. **Create the Destination.** `createDestination` — `POST /destinations` with the connection
   details for your own store. Supported types are Postgres, BigQuery, Snowflake, Redshift and S3 —
   the data lands in **your** infrastructure, not Supaglue's. `getDestinations` /
   `updateDestination` manage it afterwards.
2. **Define what to sync.** `createSyncConfig` — `POST /sync_configs` binding a
   `destination_id` and a `provider_id`, with `default_config` (sync strategy, period in seconds)
   and the `common_objects` / `standard_objects` / `custom_objects` / `entities` to pull.
   `getSyncConfigs` lists them; `updateSyncConfig` changes them.
3. **Override per customer where needed.** `upsertConnectionSyncConfig` —
   `PUT /connection_sync_configs` sets a single customer's connection apart from the default
   (different objects, different cadence). Safe to repeat.
4. **Watch it run.** `getSyncs` — `GET /syncs` shows current state per connection;
   `getSyncRuns` — `GET /sync-runs` is the run history with status and error text.
5. **Control it.** `triggerSync` — `POST /syncs/_trigger` forces a run now (use after a config
   change so you are not waiting on the schedule). `pauseSync` — `POST /syncs/_pause` and
   `resumeSync` — `POST /syncs/_resume` stop and restart it.
6. **React, don't poll.** `sync.complete` fires with a `result` of SUCCESS or ERROR, and
   `sync.paused` carries `run_id`, `connection_id`, `customer_id`, `provider_name`, `object_type`,
   `object` and `pause_reason`. See `asyncapi/supaglue-webhooks.yml`. Process within 15 seconds;
   deliveries are Svix-signed and retried with exponential backoff for up to 90 days of retention.

## Rules

- After a sync lands, unified reads can be served from the warehouse with `read_from_cache=true` —
  that is the point of the Destination. Before the first successful run, that flag returns nothing
  useful.
- `pauseSync` and `triggerSync` are POST verbs with no idempotency key; triggering twice queues two
  runs.
- A paused sync stays paused: nothing in the contract auto-resumes it, so treat `sync.paused` as an
  event that requires action.
- Every Management API error is the standard `{"errors":[{...}]}` array —
  see `errors/supaglue-problem-types.yml`.
