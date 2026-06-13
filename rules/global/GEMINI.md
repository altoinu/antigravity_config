# Stylistic Preferences
* Always retain existing code comments and notes. If making changes to a comment, explain the clear reasoning first.
* When defining objects or lists of properties, keep them in alphabetical order unless a custom order is explicitly necessary for clarity.

# Code Modification Constraints
* Only change the section of the code explicitly related to what is being discussed. Do not make unnecessary changes to unrelated sections.
* Do not simply remove or heavily modify existing parts of the code unless specifically asked or strictly required for the update. Explain the reasoning clearly before modifying or removing existing code.
* Do not make assumptions about data types (e.g., changing a variable from a string to a number just because its column name contains "id"). Explain the reasoning first if an update is needed.
* If the internal file representation seems incomplete or optimized, notify the user and ask for the full version before proceeding with modifications.

# NestJS & Database Patterns
* Enforce a strict separation between internal database Entities (representing the full database model/service layer) and public-facing DTOs (defining the public API contract/controller layer).
* If a controller endpoint attempts to return a full Entity object directly, flag it and remind the user to map the Entity to a Response DTO (using plainToInstance with @Expose) to prevent sensitive data leaks.
* Use `decimal.js` for handling monetary decimal values. Use `NUMERIC(12, 2)` for PostgreSQL storage, map rows to `new Decimal(row.amount)`, use `.toFixed(2)` for API responses, and validate inputs using `@Matches(/^\d+(\.\d{1,2})?$/)`.

# Workflow Strategy
* When making or updating multiple files, address each one step-by-step from simple/basic setup up to a complete configuration. Address unit tests alongside the implementation.
* If any instructions or provided materials are unclear or ambiguous, ask for clarification instead of making assumptions.
* Maintain a running list of out-of-scope follow-up tasks and remind the user of them at a natural stopping point.
