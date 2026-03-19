# The Life of a Project: MADLABS Project Launch Guide

This document defines how we transition from a "Project Idea" to a "Live Product" at MADLABS. This applies to new **SaaS Products**, **Websites**, and **Internal Utilities**.

---

## 🏗️ Phase 1: Conceptualization (The "Birth")
**Who:** CEO + COO + BA
**Goal:** Define the business value and feasibility.
1. **Business Proposal:** Draft a short doc (or GitHub Discussion) explaining the target market and ROI.
2. **Visual/Brand Brief (Websites):** COO defines the "Look and Feel" and interactive requirements.
3. **Approval:** CTO confirms the idea fits within the MADLABS tech stack.

---

## 📐 Phase 2: Architecture & Design (The "Blueprint")
**Who:** CTO + Senior BA + Tech Lead
**Goal:** Define the technical and functional requirements.
1. **PRD (Product Requirements Document):** BA drafts the high-level feature list.
2. **Technical Design Doc (TDD):** CTO/TL defines the stack, data model, and API contracts.
3. **Prototype/Figma:** Design team (if available) or COO approves the UI layout.
4. **Planning Mode:** Use the `enter_plan_mode` protocol to create a multi-sprint roadmap.

---

## 🚀 Phase 3: Provisioning (The "Foundation")
**Who:** Senior DevOps + CTO
**Goal:** Setup the environment.
1. **Repository Setup:** Create the repo using the `madlabs-saas-template` (for SaaS) or a standard Vite/React template (for Web).
2. **Infra-as-Code (IaC):** DevOps adds the new project to `MAD-gcp-infra` (Cloud Run, Cloud SQL, etc.).
3. **CI/CD:** Configure GitHub Actions for auto-deployment to the **Staging** environment.

---

## 🛠️ Phase 4: Sprint 0 (The "Basecamp")
**Who:** Junior / Intern Developers
**Goal:** Get to "Hello World" in production.
1. **Boilerplate:** Implement the baseline (Auth, Theme, Database connection).
2. **Multi-Tenancy:** (For SaaS) Ensure the `companyId` logic is implemented from day one.
3. **QA Baseline:** QA verifies that the app is reachable and basic navigation works.

---

## 🏃 Phase 5: MVP Iteration (The "Growth")
**Who:** Entire Team
**Goal:** Build the Minimum Viable Product.
1. **Workflow Shift:** Once the base is built, transition to the **[LIFE_OF_A_TASK.md](./LIFE_OF_A_TASK.md)** workflow.
2. **Sprints:** Focused 2-week cycles to deliver the core feature set defined in Phase 2.

---

## 🏁 Phase 6: Launch & Handoff (The "Go-Live")
**Who:** CTO + CEO + Senior QA
**Goal:** Final production push.
1. **Security Audit:** Senior DevOps/CTO performs a final secrets and permission check.
2. **Performance Audit:** Senior QA runs Lighthouse/Load tests.
3. **Marketing Launch:** COO/CEO triggers the go-to-market strategy.
4. **Archive Design:** Move planning docs to the `docs/` folder in the project repo.

---
*Last Updated: 2026-03-18*
*Owner: Staff PM*
