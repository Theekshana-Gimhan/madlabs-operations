# UAT Feedback Triage Template (MADLABS)

## 1. Feedback Metadata
- **Product:** [Simpala HR / MKS / ACMS]
- **Client/User:** [Name / Role]
- **Date Received:** [YYYY-MM-DD]
- **Source:** [Email / Meeting / WhatsApp / Form]

---

## 2. Raw Feedback / Observation
*Describe exactly what the user said or did. Include screenshots or loom links if available.*
> [Insert raw text here]

---

## 3. BA Triage & Impact Analysis
- **Category:** 
    - [ ] **Bug:** System not working as per original Specs.
    - [ ] **UI/UX Polish:** Working but hard to use.
    - [ ] **Change Request:** New requirement not in original Scope.
- **Severity:**
    - [ ] **S0 (Blocker):** Data loss, Security risk, or Process stopped.
    - [ ] **S1 (Major):** Workaround exists but is painful.
    - [ ] **S2 (Minor):** Cosmetic or non-critical.
- **Business Value:** [1-2 sentences on why this matters to the client's ROI].

---

## 4. Refined Task (For GitHub Issue)
*The BA must translate the feedback into a technical requirement for the Devs.*

### **Title:** [e.g., FIX: Payroll Export fails for employees with special characters]
- **User Problem:** [Who] needs [What] because [Why].
- **Acceptance Criteria (Gherkin):**
    - `Given... When... Then...`
- **Related Module:** [e.g., Backend / Payroll / Export]

---

## 5. Decision Log
- [ ] **Approved for Sprint:** (Move to `Ready` in Portfolio).
- [ ] **Deferred to Backlog:** (Move to `Backlog` in Portfolio).
- [ ] **Rejected:** (Reason: Out of scope or expected behavior).

---
*Last Updated: 2026-03-18*
*Owner: Senior Business Analyst*
