---
name: Fulfil a medication refill order
description: Retrieve a pending refill order, add line items, send the eScript, and complete the order in the pharmacy workflow.
api: openapi/medadvisor-pharmacy-unified-openapi.json
operations: [Account_LoginPharmacy, RefillOrder_GetPendingOrder, RefillOrder_AddLineItem, RefillOrder_SendEScript, RefillOrder_Complete]
---

# Fulfil a medication refill order

## Auth
Obtain and send a JWT bearer token (`Account_LoginPharmacy`).

## Steps
1. `GET /api/v1/RefillOrder/PendingOrder/{orderId}` (`RefillOrder_GetPendingOrder`) - load the pending order.
2. `POST /api/v1/RefillOrder/LineItem/{orderId}` (`RefillOrder_AddLineItem`) - add/adjust line items.
3. `POST /api/v1/RefillOrder/SendEScript` (`RefillOrder_SendEScript`) - attach/send the eScript token.
4. `POST /api/v1/RefillOrder/Complete` (`RefillOrder_Complete`) - complete the order.

## Rules
- Refunds/returns use `RefillOrder_RefundOrder` / `RefillOrder_ReturnToStock` - separate, auditable actions.
- Writes are not idempotent; verify order state via step 1 before re-issuing a completion.
