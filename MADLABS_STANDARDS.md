# MADLABS Engineering Standards & Architectural Mandates

## 1. Core Philosophy: "Clean, Typed, and Tested"
At MADLABS, we value maintainability over cleverness. Every line of code must be written with the next engineer in mind.

### The "Universal Contracts" (Mandatory for ALL Projects)
1. **Plan First:** No implementation starts without an approved plan and Gherkin-style Acceptance Criteria.
2. **Type Safety:** `noImplicitAny` is non-negotiable. Use `Zod` (TS) or `FluentValidation` (.NET) for all runtime validation.
3. **Standard API Response:** All APIs must follow the MADLABS Response Schema (see Section 3).
4. **Fire-and-Forget Auditing:** Critical business actions must be audited using the standard Audit Schema.
5. **TDD (Test Driven Development):** Write the test, watch it fail, implement the fix, watch it pass.

---

## 2. Architectural Modules (Optional / Per-Project)

### Module: Multi-Tenancy (SaaS Products)
- **Mandate:** Data isolation must be enforced at the lowest possible level.
- **Implementation:** 
    - Prefer **ORM-level global filters** (e.g., EF Core `HasQueryFilter` or Prisma Extensions).
    - If ORM filters are unavailable, use middleware to inject `tenantId` into every service call.
- **Isolation Wall:** Every database operation must include a tenant filter.

### Module: Financial Precision (Payroll/Fintech)
- **Mandate:** Never use `float`, `double`, or `number` for currency.
- **Implementation:** Use `decimal(18,2)` in DB and `Decimal.js` (Node) or `decimal` (C#) in code.

### Module: Complex RBAC
- **Mandate:** Provide a **Permission Diagnosis** tool to inspect a user's effective permissions and resolve access blockers.

---

## 3. Universal API Contract

All MADLABS APIs must return this standardized JSON structure:

### Success Response
```json
{
  "data": { ... },
  "meta": { "total": 100, "page": 1 } // meta is optional for pagination
}
```

### Error Response
```json
{
  "error": {
    "code": "STRING_CODE",
    "message": "Human readable message for developers",
    "details": [
      { "field": "email", "message": "Invalid email format" }
    ]
  }
}
```

**Standard Error Codes:** `BAD_REQUEST`, `UNAUTHORIZED`, `FORBIDDEN`, `NOT_FOUND`, `CONFLICT`, `INTERNAL_ERROR`.

---

## 4. Universal Audit Schema

Every `AuditLog` table/collection must at least contain:
- `userId`: The person who did the action.
- `action`: String constant (e.g., `USER_LOGIN`, `PAYROLL_RUN`).
- `entityType`: The module affected (e.g., `Employee`, `KPI`).
- `entityId`: (Optional) The specific record ID.
- `details`: (JSON/JSONB) The "Before/After" snapshot or specific metadata.
- `timestamp`: UTC time.
- `ipAddress` & `userAgent`: For security forensics.

---

## 5. The "Definition of Done" (DoD)
A task is NOT finished until:
1. [ ] Code follows **Clean Architecture** patterns.
2. [ ] **Validation** schemas are implemented for all inputs.
3. [ ] **Unit and Integration tests** are passing in CI.
4. [ ] **Acceptance Criteria (Gherkin)** are manually or automatically verified.
5. [ ] **Documentation** (JSDoc/Swagger/Markdown) is updated.
6. [ ] **Lint & Typecheck** pass without warnings.

---
*Last Updated: 2026-03-18*
*Owner: CTO / Staff PM*
