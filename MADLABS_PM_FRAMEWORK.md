# MADLABS Standard Project Management Framework (MSPF)

## 1. Governance & Tooling
- **Primary Tool:** GitHub Projects (Free Tier).
- **Structure:** One **"MADLABS Master Portfolio"** Project for the CEO/CTO to view all products, and individual **"Delivery Boards"** for each high-priority project (e.g., Simpala HR, MKS).
- **Communication:** GitHub Issues for all task-level communication. No "private" Slack/Teams decisions should go unrecorded in the Issue.

---

## 2. The MADLABS Standard SDLC (Software Development Life Cycle)

### Phase 1: Product Discovery (BA + CEO + CTO)
- **Goal:** Define the "Why" and "What."
- **Output:** A GitHub Issue with a clear **User Problem Statement** and **Gherkin-style Acceptance Criteria (AC)**.
- **Role of BA:** Responsible for drafting the AC and ensuring it aligns with business needs.

### Phase 2: Technical Refinement (Tech Lead + CTO)
- **Goal:** Define the "How" (Plan-First).
- **Output:** An **Implementation Plan** added to the Issue. 
- **Requirement:** Must identify affected modules, security/compliance risks (EPF/ETF), and data migration impact.

### Phase 3: Execution & TDD (Junior/Intern Devs)
- **Goal:** Build and Test.
- **Workflow:** 
    1. Create Branch (e.g., `feat/issue-123-payroll-fix`).
    2. Write failing test case based on AC.
    3. Implement fix (following `MADLABS_STANDARDS.md`).
    4. Run local verification (Lint, Typecheck, Test).

### Phase 4: Quality Assurance (QA Senior)
- **Goal:** Independent Verification.
- **Workflow:** 
    - Verify AC on a **Staging/UAT Environment**.
    - Label Issue as `qa-passed`.
    - If failed, move to `Reopened` with clear reproduction steps.

### Phase 5: Deployment & Operations (Senior DevOps)
- **Goal:** Promotion to Production.
- **Workflow:** Merge to `main` -> Auto-deploy via GCP Cloud Build -> Verify Health Checks.

---

## 3. Work Item Standards (Issue Template)
Every task must use the following structure:

### **[Title]: Brief, Action-Oriented (e.g., "Implement Cache Invalidation for Employee Profile")**
- **User Problem:** [Who] needs [What] because [Why].
- **Acceptance Criteria:**
    - `Given... When... Then...`
- **Technical Plan:** (To be drafted by Dev, approved by TL).
- **Testing Strategy:** [Unit/Integration/Manual].
- **Definition of Done:** 
    - [ ] Typecheck pass.
    - [ ] TDD Tests pass.
    - [ ] Multi-tenant isolation verified.

---

## 4. Meeting Cadence (Zero-Meeting Policy)
To maximize flow, we prefer **Asynchronous Management**:
- **Daily Async Standup:** Post status in the PM Intern's tracking thread: "Yesterday I did X, Today I'm doing Y, Blocked by Z."
- **Weekly Sprint Review (CEO/COO/CTO):** 30-minute demo of "Live" features.
- **Triage Session (BA/QA/TL):** Weekly 15-minute sync to prioritize the next 5 items in the backlog.

---

## 5. Branching & Release Strategy
- **`main`**: Production-ready code only.
- **`develop`**: Integration branch for UAT.
- **`feat/*` or `fix/*`**: Ephemeral branches for single issues.
- **Releases:** Tags (e.g., `v1.2.0-uat`) are used for staging promotions.

---
*Last Updated: 2026-03-18*
*Owner: Staff PM*
