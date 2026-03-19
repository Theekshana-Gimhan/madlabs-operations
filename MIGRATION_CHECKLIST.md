# MADLABS Standards Migration Checklist

Use this checklist to track the alignment of "Legacy" projects with the new MADLABS MASTER Standards.

## 📊 Project Status Overview

| Project | Phase 1 (Governance) | Phase 2 (AI/Legal) | Phase 3 (Technical) | Status |
| :--- | :---: | :---: | :---: | :--- |
| **Simpala HR** | 🟡 | 🔴 | 🔴 | In Progress |
| **MKS (KPI)** | 🔴 | 🔴 | 🔴 | Pending |
| **ACMS** | 🔴 | 🔴 | 🔴 | Pending |

---

## 🟢 Phase 1: Governance & Management
*Goal: Align the project with the MADLABS project management framework.*

- [ ] **Master Portfolio Integration:** All active issues moved to the GitHub Master Portfolio.
- [ ] **Gherkin AC:** Backlog refined with "Given/When/Then" acceptance criteria.
- [ ] **Product Tagging:** All items tagged with the correct `Product` and `Priority`.
- [ ] **Workflow Adoption:** Team is moving cards through Phase 1-5 (Discovery -> Done).

## 🟡 Phase 2: AI Guardrails & Legal
*Goal: Inject standards into the developer's environment (Non-Breaking).*

- [ ] **LICENSE:** Added the MADLABS Proprietary License to root.
- [ ] **AI Guardrails:** `.cursorrules` added to root.
- [ ] **Copilot Config:** `.github/copilot-instructions.md` added to root.
- [ ] **CONTRIBUTING.md:** Updated to mandate TDD and Clean Architecture.

## 🔴 Phase 3: Technical Alignment
*Goal: Surgical code refactors to meet the MADLABS Engineering Constitution.*

- [ ] **Standard API Response:** All endpoints follow the `{ data, error }` JSON schema.
- [ ] **Automated Multi-Tenancy:** ORM-level global filters implemented (No manual `tenantId` checks).
- [ ] **Monetary Precision:** All currency fields converted to `Decimal` (No floats/numbers).
- [ ] **Standard Auditing:** Audit logs follow the universal schema (`userId`, `action`, `details`).
- [ ] **TDD Baseline:** CI/CD gates enforced for all new pull requests.

---

## 🛠️ How to use this Checklist
1. **Tech Lead:** Update the "Project Status Overview" table every Friday.
2. **PM Intern:** Ensure Phase 1 is complete for all high-priority projects.
3. **Junior Devs:** Focus on Phase 2 files immediately to "prime" your Copilot.

---
*Last Updated: 2026-03-18*
*Owner: Staff PM / Tech Lead*
