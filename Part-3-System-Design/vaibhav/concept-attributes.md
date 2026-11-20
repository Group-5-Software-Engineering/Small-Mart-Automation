# 6. Concept Attribute Tables

Following the intent of Marsic Table 2-8, these are candidate descriptive attributes rather than full database schemas. Types and constraints are design proposals.

## 6.1 Catalog and Inventory

| Concept | Attribute | Candidate type | Constraint / purpose |
|---|---|---|---|
| Product | sku | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Product | name | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Product | price | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Product | reorderThreshold | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockBatch | batchId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockBatch | quantity | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockBatch | expiryDate | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockMovement | movementId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockMovement | quantityDelta | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockMovement | reason | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Supplier | supplierId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Supplier | name | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| PurchaseOrder | orderId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| PurchaseOrder | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| PurchaseOrder | proposedQty | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| InventoryAlert | alertId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| InventoryAlert | alertType | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| InventoryAlert | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |

## 6.2 Point of Sale and Returns

| Concept | Attribute | Candidate type | Constraint / purpose |
|---|---|---|---|
| Sale | saleId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Sale | timestamp | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Sale | total | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Sale | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| SaleLine | quantity | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| SaleLine | unitPrice | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Product | sku | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Product | price | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Payment | paymentId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Payment | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Payment | amount | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Receipt | receiptNo | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Receipt | issuedAt | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Return | returnId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Return | reason | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Return | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockMovement | movementId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| StockMovement | quantityDelta | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |

## 6.3 Administration and Oversight

| Concept | Attribute | Candidate type | Constraint / purpose |
|---|---|---|---|
| Employee | employeeId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Employee | name | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Employee | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Role | roleId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Role | permissionSet | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Shift | shiftId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Shift | start | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Shift | end | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| AuditEvent | eventId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| AuditEvent | action | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| AuditEvent | timestamp | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Report | reportId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Report | period | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Report | type | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |

## 6.4 Loyalty and Offline Reconciliation

| Concept | Attribute | Candidate type | Constraint / purpose |
|---|---|---|---|
| LoyaltyAccount | accountId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| LoyaltyAccount | pointsBalance | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| LoyaltyEntry | entryId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| LoyaltyEntry | pointsDelta | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Sale | saleId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| Sale | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| OfflineTransaction | queueId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| OfflineTransaction | clientTxnId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| OfflineTransaction | status | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| SyncAttempt | attemptId | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
| SyncAttempt | result | Identifier / decimal / date / text as appropriate | Required or validated by the relevant business rule |
