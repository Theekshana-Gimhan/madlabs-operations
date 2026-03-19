# MADLABS Project Management Memory (PMM)

## 1. Executive Summary
MADLABS is a scaling software solution startup. The workspace has been reorganized into categorized directories: **SAAS**, **Utilities**, and **WEB-react**.

## 2. Strategic Priorities (North Star: Simpala HR)

### SaaS Products (`D:\dev\SAAS`)
| Product | Priority | Status | Current Focus / Milestone |
| :--- | :--- | :--- | :--- |
| **Simpala HR (HR)** | **High** | In Development | **Track A (Stabilization):** Cache, Timezone, Payroll, Leave. |
| **MAD_KPI_SOLUTION (MKS)** | Medium | UAT / Launch | **Phase 7:** Production Deployment & UAT Sign-off. |
| **Agent Commission (ACMS)** | Medium | UAT | **Feedback Loop:** Triage client feedback for Prod promotion. |
| **FinTrack** | Low | Initial Stage | Backlog refinement. |
| **AI Persona Simulator** | Low | Initial Stage | Infrastructure stabilization. |
| **EduNexus** | Ideas | Conceptual | Awaiting development kickoff. |

## 3. Operational Roadmap (Next 14 Days)

### Week 1: Stabilization & Triage
- **[HR]** Junior Devs to implement Cache Invalidation hardening and Timezone standardization.
- **[MKS/ACMS]** Senior BA + QA to complete UAT regression cycles.
- **[Infra]** Senior DevOps to verify Production auto-scaling and monitoring for Simpala HR.

### Week 2: Quality & Launch
- **[HR]** Start Track B (API validation consistency & E2E happy paths).
- **[MKS]** Final Production Cutover (DNS mapping, SSL, Production Seeding).
- **[ACMS]** Finalize UAT bug fixes and schedule Production release.

## 4. Organizational Structure

### Web Properties (`D:\dev\WEB-react`)
- **mad-web** (Company site)
- **Kiyanna-web**
- **GLP-web**
- **NCCYW**
- **VXL_Global**
- **vxl-website**
- **microsite game** (Idea)

### Infrastructure & Utilities (`D:\dev\Utilities`)
- **MAD-gcp-infra**: Terraform configurations for GCP.
- **MD2PDF-Desktop**: Markdown to PDF conversion utility.
- **Cybersource Payment Plugin**: Custom WordPress integration.
- **MADLABS MASTER Template**: Standardized GitHub Template for all projects.

## 5. Organizational Structure
**Budget for Tools:** $0 (Strictly Open Source / GitHub Free Tier).

| Role | Count | Expertise |
| :--- | :--- | :--- |
| **CEO** | 1 | Business & Sales |
| **COO** | 1 | Marketing, Branding, Advertising |
| **CTO (You)** | 1 | AI Automation & Software Architecture |
| **Tech Lead / Auditor** | 1 | External Senior Oversight |
| **Senior DevOps** | 1 | GCP / Terraform / CI/CD |
| **Senior QA** | 1 | Quality Assurance |
| **Senior BA** | 1 | Business Analysis / Requirements |
| **Junior Devs** | 2 | Feature implementation |
| **Intern Devs** | 2 | Learning / Support |
| **PM Intern** | 1 | Project coordination |

## 6. Operational Mandates
1. **GitHub-Centric:** Use Issues, Projects, and Milestones for all tracking.
2. **Standardization:** All new projects must derive from `MADLABS MASTER Template`.
3. **Architecture:** Clean Architecture, Type Safety (Zod), and TDD are mandatory (as per `MADLABS_STANDARDS.md`).

---
*Last Updated: 2026-03-18*
