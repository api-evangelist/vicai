---
name: Sync ERP masterdata into Vic.ai
description: Push and reconcile General Ledger accounts, vendors, and dimensions from your ERP into Vic.ai so invoices can be auto-coded.
api: openapi/vicai-openapi-original.json
operations: [obtainToken, upsertAccount, synchronizeAccounts, upsertVendor, synchronizeVendors, upsertDimension, synchronizeDimensions]
---

# Sync ERP masterdata into Vic.ai

Vic.ai needs a current copy of your ERP masterdata (accounts, vendors, dimensions) to code invoices. Masterdata is company-scoped and sync is **explicit** — your integration decides the order and must avoid ping-pong loops (do not call a synchronize function from a webhook handler that was itself triggered by a sync).

## Auth
1. `obtainToken` — `POST /v0/token` with `{ client_id, client_secret }`. Store the returned `access_token` (JWT, `expires_in` 3600s; may exceed 530 chars). Send `Authorization: Bearer <access_token>` on every call.

## Steps
1. `upsertAccount` — `PUT /v0/accounts/{id}` for each GL account (idempotent upsert keyed by your ERP id).
2. `upsertVendor` — `PUT /v0/vendors/{id}` for each vendor.
3. `upsertDimension` — `PUT /v0/dimensions/{id}` for each business dimension.
4. `synchronizeAccounts` / `synchronizeVendors` / `synchronizeDimensions` — `POST .../synchronize` to reconcile the full set so Vic.ai can prune records removed in your ERP.

## Conventions
- Pagination is cursor-based: pass `limit` (max 100) and `cursor` (from the `X-next` response field) when listing.
- Rate limit: 500 requests / 10s per OAuth client id → `429`. On `429`, back off and capture the request id from the response headers for support.
- There is **no idempotency-key header**; the `PUT` upserts are naturally idempotent by resource id, but `POST` create/synchronize calls are not — guard against duplicates yourself.
- Errors: `{ code, message }` (v0) — see errors/vicai-error-codes.yml.
