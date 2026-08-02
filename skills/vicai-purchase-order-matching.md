---
name: Sync purchase orders for invoice matching
description: Push purchase orders and line items from your ERP into Vic.ai so incoming invoices are automatically matched, then read match results and close fulfilled POs.
api: openapi/vicai-openapi-original.json
operations: [obtainToken, createPurchaseOrder, synchronizePurchaseOrders, createPurchaseOrderLineItem, closePurchaseOrder, getInvoice]
---

# Sync purchase orders for invoice matching

Vic matches incoming invoices to purchase orders on PO number, vendor, amounts, quantities, and line-level data, then flags discrepancies for review. Your job as integrator is to keep POs current and react to match results.

## Auth
1. `obtainToken` — `POST /v0/token`; use the Bearer JWT on all calls.

## Keep POs synchronized
2. `createPurchaseOrder` — `POST /v0/purchaseOrders` to create a PO in Vic reflecting your ERP.
3. `createPurchaseOrderLineItem` — `POST /v0/purchaseOrderLineItems` to add line items (update received quantities as goods arrive).
4. `synchronizePurchaseOrders` — `POST /v0/purchaseOrders/synchronize` to reconcile the full PO set.

## React to match results
5. `getInvoice` — `GET /v0/invoices/{id}` returns match data on the invoice payload; invoice webhooks also carry it. Record matches/discrepancies in your ERP.
6. `closePurchaseOrder` — `POST /v0/purchaseOrders/{purchaseOrderId}/close` once a PO is fully fulfilled (reopen with `openPurchaseOrder`).

## Conventions
- Cursor pagination (`limit` max 100, `cursor` from `X-next`) when listing POs.
- Rate limit 500/10s per client id; handle `429` with the request id from headers.
- No idempotency-key header — dedupe PO creates by your ERP reference; `PUT` updates are id-keyed.
- Optional `billOfLading` / `deliveryNote` references are accepted on PO receipt lines (added 2026-07-19).
