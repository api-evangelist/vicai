---
name: Post an approved invoice from Vic.ai to your ERP
description: Subscribe to invoice webhooks, receive the invoice_post event, write it to your ERP, and complete the asynchronous confirm/reject handshake.
api: openapi/vicai-openapi-original.json
operations: [obtainToken, createSubscription, subscribe, listWebhookEvents, getWebhookEvent, getInvoice, confirmInvoice, rejectInvoice]
---

# Post an approved invoice from Vic.ai to your ERP

Posting sends a finalized, approved invoice from Vic to your ERP. Vic delivers a webhook with the invoice data; your system writes it into the ERP and calls back to **confirm** or **reject**. This is an asynchronous handshake.

## Auth
1. `obtainToken` — `POST /v0/token` with `{ client_id, client_secret }`; use the Bearer JWT on all calls.

## Set up delivery
2. Subscribe to events pointed at `https://<yourCallbackUrl>/events`:
   - V2 (recommended, multi-subscription, company-scoped): `createSubscription` — `POST /v2/companies/{company_id}/subscriptions`.
   - V0 (single subscription per company): `subscribe` — `PUT /v0/subscription`.
   - Subscribe to `invoice_post` (and `invoice_transfer`, `invoice_updated`, `invoice_rejected`) or `["all"]` (must be set alone; not recommended in production).

## Handle the post
3. On the inbound `invoice_post` (or `invoice_transfer`) webhook POST, read the invoice payload. Optionally re-fetch with `getInvoice` — `GET /v0/invoices/{id}`.
4. Write the invoice into your ERP.
5. Close the handshake:
   - Success: `confirmInvoice` — `POST /v0/invoices/{id}/confirm`.
   - Failure: `rejectInvoice` — `POST /v0/invoices/{id}/reject`.
6. Audit/inspect delivery history with `listWebhookEvents` (`GET /v0/webhooks/events`) and `getWebhookEvent` (`GET /v0/webhooks/events/{event_id}`).

## Conventions
- Do not call a synchronize function from inside a webhook handler triggered by a sync (avoid ping-pong loops).
- Rate limit 500/10s per client id; `429` returns a request id in headers.
- No idempotency-key header — dedupe on the invoice id and webhook event id yourself.
