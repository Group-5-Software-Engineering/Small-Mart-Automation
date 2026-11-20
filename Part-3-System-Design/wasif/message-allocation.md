# 9. Additional Responsibility Description Tables — Message Allocation

These tables extend the initial responsibilities to message-level collaborators, adapting Marsic Table 2-9. The assignment favors responsibility allocation to the object with the relevant information and avoids making a single controller responsible for every business rule.

| Operation / message | Responsible class | Collaborator | Rationale / safeguard |
|---|---|---|---|
| validate SKU and product details | CatalogService | ProductRepository | Product owns business attributes; repository retrieves record |
| receive shipment | InventoryService | StockLedger | Record stock batch and quantity atomically |
| calculate checkout total | SalesService | CatalogRepository | Use authoritative price and applicable tax/discount rules |
| authorize payment | PaymentService | SalesService | Do not commit a rejected payment |
| post sale stock deduction | StockLedger | SalesRepository | Sale and quantity movement must commit together |
| validate return eligibility | ReturnsService | SalesRepository | Prevent excessive or unauthorized returns |
| generate inventory alerts | AlertService | InventoryRepository | Compare quantity with threshold and expiry |
| approve purchase order | ReorderService | PurchaseOrderRepository | Manager authorization and order status |
| maintain employee permissions | EmployeeService | RoleRepository | Restrict privileged operations |
| compile operational report | ReportingService | SalesRepository | Read-only aggregation for manager |
| record exception review | AuditService | AuditRepository | Preserve actor, timestamp and outcome |
| apply loyalty redemption | LoyaltyService | LoyaltyRepository | Prevent negative or double-applied points |
| deduplicate queued sale | SyncCoordinator | SalesRepository | Idempotent unique transaction handling |
