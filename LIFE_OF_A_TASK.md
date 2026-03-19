# The Life of a Task: MADLABS Workflow Guide

This document defines the journey of every feature, bug fix, or improvement at MADLABS. Follow these stages to ensure high-quality, typed, and tested delivery.

---

## 🟢 Stage 1: Discovery (The "What")
**Who:** Senior Business Analyst (BA) + CEO
**Goal:** Define the user value and requirements.
1. **Action:** Create a GitHub Issue in the relevant repository.
2. **Format:** Use the `UAT_FEEDBACK_TRIAGE_TEMPLATE.md`.
3. **Requirement:** Must include **Gherkin-style Acceptance Criteria (AC)** (Given/When/Then).
4. **Board:** Add to the `MADLABS Master Portfolio` in the **Backlog** column.

---

## 🟡 Stage 2: Refinement (The "How")
**Who:** Tech Lead / CTO
**Goal:** Define the technical approach and risk.
1. **Action:** Review the Backlog. If AC is clear, draft a **Technical Implementation Plan** in the issue comments.
2. **Standard:** Follow `MADLABS_STANDARDS.md` (Clean Architecture, Zod validation, Multi-tenancy).
3. **Board:** Move to the **Ready** column. This signals "Approved for Development."

---

## 🔵 Stage 3: Execution (The "Build")
**Who:** Junior / Intern Developers
**Goal:** Build, Test, and Verify.
1. **Action:** Assign yourself to a **Ready** issue and move it to **In Progress**.
2. **TDD:** Write failing tests first, then implement the code.
3. **Delivery:** Open a Pull Request (PR) and link it to the issue (e.g., `Closes #123`).
4. **Board:** GitHub automation moves the card to **In Review**.

---

## 🟣 Stage 4: Verification (The "Check")
**Who:** Senior QA + Tech Lead
**Goal:** Independent quality gate.
1. **Review:** Tech Lead reviews code and merges the PR.
2. **QA:** Senior QA sees the card in the **QA / UAT** column.
3. **Test:** Verify AC in the **Staging environment**. 
4. **Sign-off:** Add a "QA Passed" comment and move the card to **Done**.

---

## ⚪ Stage 5: Operations (The "Rhythm")
**Who:** PM Intern
**Goal:** Maintain the flow and update stakeholders.
1. **Monitor:** Ensure every `In Progress` task has an assignee and a `Product` tag.
2. **Escalate:** Ping the CTO if a task is stuck in `In Review` or `QA` for >48 hours.
3. **Archive:** Every Friday, archive the **Done** column and update the `MADLABS_PM_MEMORY.md`.

---
*Last Updated: 2026-03-18*
*Owner: Staff PM*
