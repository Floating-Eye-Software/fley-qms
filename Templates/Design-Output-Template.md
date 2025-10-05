## 📄 Template: *Work Unit Design Output Record*

### 1. General Information

| Field                    | Description                                              | Example                    |
| ------------------------ | -------------------------------------------------------- | -------------------------- |
| Work Unit ID             | Unique identifier (issue number, PR ID, or internal ref) | `ISSUE-142`                |
| Title                    | Brief name of the work unit                              | “Add login audit logging”  |
| Type                     | ☐ Feature ☐ Bug Fix ☐ Doc ☐ Process ☐ Research           | Feature                    |
| Responsible Person(s)    | Who performed or led the work                            | J. Smith                   |
| Date Completed           |                                                          | 2025-10-04                 |
| Linked Repos / Artifacts | URLs or references                                       | GitHub Issue #142, PR #219 |

---

### 2. Design Inputs (Reference Only)

| Field                                  | Description                                        | Example                                   |
| -------------------------------------- | -------------------------------------------------- | ----------------------------------------- |
| Source of Requirement                  | Customer request, internal improvement, risk, etc. | Internal audit finding                    |
| Input Reference(s)                     | Issue ID, meeting note, user story, spec           | #134, meeting 2025-09-10                  |
| Acceptance Criteria / Expected Outcome | What success looks like                            | Audit logs created for all login attempts |

---

### 3. Design Outputs

| Field                       | Description                              | Example                                                  |
| --------------------------- | ---------------------------------------- | -------------------------------------------------------- |
| Deliverables Produced       | List tangible outputs                    | Updated `auth_service.py`, new `audit_log.md` doc        |
| Verification / Testing Done | How output was verified                  | Unit tests passed (pytest report #111), peer review done |
| Related Documents           | Specs, procedures, training docs updated | SOP-07 “User Access Control”                             |
| Quality Criteria Met?       | ☐ Yes ☐ No (explain below)               | ☑ Yes                                                    |
| Evidence of Conformance     | Attach links, screenshots, or logs       | GitHub Actions CI log, test coverage report              |

---

### 4. Review & Approval

| Field               | Description                                    | Example                 |
| ------------------- | ---------------------------------------------- | ----------------------- |
| Reviewer            | Person verifying adequacy of outputs           | M. Patel                |
| Review Date         |                                                | 2025-10-05              |
| Findings / Comments |                                                | Minor doc edit required |
| Approval            | ☐ Approved ☐ Conditionally Approved ☐ Rejected | ☑ Approved              |

---

### 5. Metrics Summary (Optional – for QMS monitoring)

| Metric                     | Value | Source                |
| -------------------------- | ----- | --------------------- |
| Lead Time (days)           | 6     | GitHub Issue timeline |
| Number of commits          | 8     | GitHub                |
| Documentation updated      | Yes   | Wiki                  |
| Defects found post-release | 0     | Issue tracker         |

---

### 6. Lessons Learned / Improvement Notes (Optional)

Short summary of any process improvement, learning, or change request that resulted from this work unit.

> e.g., “Need better log sanitization guidelines. Add to coding SOP.”

---
