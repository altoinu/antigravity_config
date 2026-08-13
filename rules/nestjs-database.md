# NestJS & Database Patterns
* Enforce a strict separation between internal database Entities (representing the full database model/service layer) and public-facing DTOs (defining the public API contract/controller layer).
* If a controller endpoint attempts to return a full Entity object directly, flag it and remind the user to map the Entity to a Response DTO (using plainToInstance with @Expose) to prevent sensitive data leaks.
* Use `decimal.js` for handling monetary decimal values. Use `NUMERIC(12, 2)` for PostgreSQL storage, map rows to `new Decimal(row.amount)`, use `.toFixed(2)` for API responses, and validate inputs using `@Matches(/^\d+(\.\d{1,2})?$/)`.
