# QP-08.05.06 — Pull Request Change Control Procedure
**Title:** Control of Design, Development, and QMS Document Changes via Pull Requests
**Revision:** 1.0
**Effective Date:** 2025-10-04
**Process Owner:** Quality Manager / DevOps Lead

---

## 1. Purpose
This procedure defines how changes to controlled work outputs, designs, and quality management system (QMS) documents are proposed, reviewed, approved, and recorded using GitHub Pull Requests (PRs).
The goal is to ensure all changes are evaluated for adequacy, correctness, and impact before release or implementation.

---

## 2. Scope
This procedure applies to:
- All software design and development work performed under the QMS
- Controlled documents such as SOPs, policies, templates, and records stored in the GitHub Wiki or QMS repositories
- Any other item designated as controlled information under the QMS

---

## 3. References
- **ISO 9001:2015**
  - Clause 7.5 – Documented Information
  - Clause 8.3.6 – Design and Development Changes
  - Clause 8.5.6 – Control of Changes
  - Clause 9.1 – Performance Evaluation
- SOP-07 Configuration Management
- WI-03 Work Unit Design Output Template

---

## 4. Definitions
| Term | Definition |
|------|-------------|
| **Pull Request (PR)** | GitHub mechanism for proposing a change from one branch to another. |
| **Change Originator** | Individual initiating the PR. |
| **Reviewer / Approver** | Authorized person verifying and approving the change before merge. |
| **Controlled Repository** | Any GitHub repository or wiki folder subject to QMS change control. |

---

## 5. Procedure

### 5.1 Initiation
1. All proposed changes to controlled items must be initiated through a Pull Request.
2. The PR description must include:
   - Purpose and scope of the change
   - Reference to related issue, requirement, or audit finding
   - Summary of verification or testing performed
3. Each PR must reference any related **Work Unit Design Output Record**.

---

### 5.2 Review and Approval
1. Every PR must be reviewed by at least one qualified **Reviewer** not directly responsible for the original change.
2. Reviewers confirm that:
   - The change meets input requirements or objectives.
   - No adverse or unintended effects are introduced.
   - Verification or testing has been completed successfully.
   - Relevant documentation (code comments, wiki, SOPs) has been updated.
3. Review comments are resolved before approval.
4. Formal approval is granted by the reviewer using GitHub’s **Approve Pull Request** action.
5. Only individuals designated as approvers in the **CODEOWNERS** file or authority matrix may approve merges to controlled branches.

---

### 5.3 Merge and Record Retention
1. Approved PRs are merged into the target branch (e.g., `main`).
2. The merge commit, review comments, and linked issues form the permanent change record.
3. Artifacts such as CI/CD results or verification reports are linked within the PR.
4. All PRs remain stored in GitHub and constitute objective evidence of change control.

---

### 5.4 Post-Implementation Verification
1. After merge, automated or manual verification confirms intended performance.
2. If any issues arise, a new corrective-action issue is opened and linked to the PR.

---

### 5.5 Emergency / Hotfix Changes
1. Urgent changes required to restore service or integrity may be merged with expedited review.
2. The justification must be documented in the PR description.
3. A retrospective review and approval are performed within 5 working days.

---

### 5.6 Metrics and Monitoring
- Number of PRs created, reviewed, and approved
- Average lead time from PR creation to merge
- Frequency of re-opened issues or rollback events
- Review of metrics occurs during Management Review (ISO 9001 § 9.3)

---

### 5.7 Application to QMS and Quality Documents
1. This PR process also applies to controlled **QMS documents**, including:
   - Standard Operating Procedures (SOPs)
   - Work Instructions (WIs)
   - Policies, manuals, templates, and forms
   - Wiki-based QMS pages or Markdown documentation
2. Changes to QMS documentation must be initiated via a Pull Request that includes:
   - Summary of proposed change and justification
   - References to related audit findings, CARs/PARs, or improvement requests
3. Review and approval must be performed by the **Process Owner** and/or **Quality Manager** as defined in the authority matrix or CODEOWNERS file.
4. The GitHub PR approval and merge history constitute the formal record of review and approval required by ISO 9001 § 7.5.2.
5. When merged:
   - The updated version becomes the current controlled document.
   - Previous versions remain accessible via GitHub history.
   - The merge commit or PR link may be noted in the QMS revision log if required.
6. Major procedural or policy changes that affect multiple processes should be referenced in a **QMS Change Notice** or **Management Review** record.

---

## 6. Records
| Record | Storage Location | Retention |
|--------|------------------|-----------|
| Pull Request (including approvals, comments, merge history) | GitHub repository | Permanent |
| Linked Work Unit Design Output Record | `/qms/design-outputs/` | 3 years minimum |
| CI/CD Verification Logs | Build system | 1 year minimum |

---

## 7. Roles and Responsibilities
| Role | Responsibility |
|------|----------------|
| **Change Originator** | Initiates PR, ensures completeness of description and evidence. |
| **Reviewer / Approver** | Reviews and approves changes for adequacy and impact. |
| **Quality Manager** | Audits PR process and ensures documentation integrity. |
| **DevOps Lead** | Maintains branch protection, CODEOWNERS, and access control settings. |

---

## 8. Related Documents
- WI-03 Work Unit Design Output Template
- SOP-07 Configuration Management
- QP-08.07 Corrective and Preventive Action Procedure

---

**End of Procedure**
