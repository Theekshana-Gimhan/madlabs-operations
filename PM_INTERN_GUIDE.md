# PM Intern Management Guide (MADLABS)

## 1. Your Goal
Your primary responsibility is to ensure the **MADLABS Master Portfolio** is the "Single Source of Truth." If a task isn't on the board, it doesn't exist.

## 2. Daily Routine (The "15-Minute Sync")
Every morning, review the board and ensure:
1. **No "Ghost" Issues:** Every issue in `In Progress` must have an **Assignee** and a **Product** tag.
2. **Stale Check:** If an issue has been in `In Review` for more than 48 hours, ping the **Tech Lead** or **CTO** for a review.
3. **QA Queue:** If an issue is in `QA / UAT`, notify the **Senior QA** that a new feature is ready for testing.
4. **Update Status:** Ensure developers are moving cards as they work. If they forget, remind them politely.

## 3. Weekly Routine (The "Friday Cleanup")
1. **Archive Done:** Move all issues in the `Done` column to "Archived" to keep the board clean.
2. **Backlog Refinement:** Ensure all new issues in the `Backlog` have a **User Problem Statement** and **Acceptance Criteria**. If missing, ask the **Senior BA** to fill them in.
3. **Metric Update:** Record the number of `Done` issues this week and share it with the **CEO/CTO** in the async status thread.

## 4. Work Item Standards
When you see a new issue, check for these 3 things. If they are missing, the issue is **NOT READY** for development:
- [ ] **Gherkin AC:** (Given/When/Then).
- [ ] **Product Tag:** (e.g., Simpala HR).
- [ ] **Priority:** (P0, P1, or P2).

## 5. Escalation Policy
Ping the **CTO** immediately if:
- A **P0 (Critical)** issue is blocked for more than 4 hours.
- A **Senior QA** reports a critical regression in a UAT product (MKS/ACMS).
- There is a conflict between the **BA** and **Tech Lead** on a requirement.

---
*Last Updated: 2026-03-18*
*Owner: Staff PM*
