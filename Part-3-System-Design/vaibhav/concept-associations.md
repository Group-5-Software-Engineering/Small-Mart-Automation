# 5. Concept Association Tables

The following tables adapt Marsic Table 2-7 by naming business relationships, their multiplicities, and the reason each association is necessary.

## 5.1 Catalog and Inventory

| Concept A | Association / cardinality | Concept B | Rationale |
|---|---|---|---|
| Product | 1 to 0..* | StockBatch | Supports linked use-case data and lifecycle. |
| Product | 1 to 0..* | StockMovement | Supports linked use-case data and lifecycle. |
| Supplier | 1 to 0..* | PurchaseOrder | Supports linked use-case data and lifecycle. |
| PurchaseOrder | 0..* items | Product | Supports linked use-case data and lifecycle. |
| Product | 1 to 0..* | InventoryAlert | Supports linked use-case data and lifecycle. |

## 5.2 Point of Sale and Returns

| Concept A | Association / cardinality | Concept B | Rationale |
|---|---|---|---|
| Sale | 1 to 1..* | SaleLine | Supports linked use-case data and lifecycle. |
| SaleLine | * to 1 | Product | Supports linked use-case data and lifecycle. |
| Sale | 1 to 0..* | Payment | Supports linked use-case data and lifecycle. |
| Sale | 1 to 0..1 | Receipt | Supports linked use-case data and lifecycle. |
| Sale | 1 to 0..* | Return | Supports linked use-case data and lifecycle. |
| Return | 1 to 0..* | StockMovement | Supports linked use-case data and lifecycle. |

## 5.3 Administration and Oversight

| Concept A | Association / cardinality | Concept B | Rationale |
|---|---|---|---|
| Employee | * to 1 | Role | Supports linked use-case data and lifecycle. |
| Employee | 1 to 0..* | Shift | Supports linked use-case data and lifecycle. |
| Employee | 1 to 0..* | AuditEvent | Supports linked use-case data and lifecycle. |
| Report | references 0..* | AuditEvent | Supports linked use-case data and lifecycle. |

## 5.4 Loyalty and Offline Reconciliation

| Concept A | Association / cardinality | Concept B | Rationale |
|---|---|---|---|
| LoyaltyAccount | 1 to 0..* | LoyaltyEntry | Supports linked use-case data and lifecycle. |
| LoyaltyEntry | 0..* to 0..1 | Sale | Supports linked use-case data and lifecycle. |
| OfflineTransaction | 0..1 to 1 | Sale | Supports linked use-case data and lifecycle. |
| OfflineTransaction | 1 to 0..* | SyncAttempt | Supports linked use-case data and lifecycle. |
