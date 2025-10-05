# QP-07.05 — Document Control Procedure
**Title:** Control of Documents and Electronic Records
**Revision:** 1.0
**Effective Date:** 2025-10-04
**Process Owner:** Quality Manager

---

## 1. Purpose
To define the controls necessary to ensure that all documents and electronic records required by the Quality Management System (QMS) are reviewed, approved, distributed, and maintained using the GitHub platform as the system of record.
This procedure also defines how electronic reviews and approvals performed through GitHub Pull Requests (PRs) are recognized as compliant electronic signatures in accordance with ISO 9001:2015 and 21 CFR Part 11.

---

## 2. Scope
This procedure applies to:
- All controlled QMS documents (SOPs, work instructions, templates, forms, policies).
- Product-related documentation maintained in the *redwitch* repository.
- Software design, development, and verification records generated within GitHub.

---

## 3. References
- **ISO 9001:2015** – Clause 7.5 Documented Information
- **21 CFR Part 11** – Electronic Records; Electronic Signatures
- **QP-08.05.06** – Pull Request Change Control Procedure
- **SOP-07** – Configuration Management

---

## 4. Definitions
| Term | Definition |
|------|-------------|
| **Controlled Document** | Any document subject to review and approval prior to use. |
| **Pull Request (PR)** | GitHub mechanism used to propose, review, and approve a change. |
| **Electronic Signature** | GitHub user identity and approval action recorded within a PR, including username, timestamp, and intent (approve/reject). |
| **Main Branch** | Repository branch containing current, approved versions of controlled documents. |
| **Draft Branch** | Temporary branch used to prepare document updates prior to approval. |

---

## 5. Procedure

### 5.1 Document Creation and Identification
1. All controlled documents shall include:
   - Document ID, title, revision, effective date, and owner.
   - Unique filename and clear folder structure (e.g., `/SOPs/`, `/Policies/`).
2. New or revised documents are created on a dedicated branch (e.g., `draft/update-SOP07`).

---

### 5.2 Review and Approval
1. Drafts are submitted for review via a **Pull Request**.
2. The PR description shall include:
   - Purpose of change
   - Summary of revisions
   - Related issues, audits, or corrective actions
3. Reviewers (Process Owners or Quality Manager) provide feedback directly in the PR.
4. When reviewers select **“Approve”** in GitHub, the system records:
   - Authenticated user ID
   - Date and time stamp
   - Meaning of signature (“Approved for release”)
   These actions constitute *electronic signatures* under **21 CFR Part 11 §§ 11.50–11.70**.
5. After approval, the PR is merged into the `main` branch by an authorized user.
   - The merged version becomes the controlled document.
   - Prior versions remain retrievable in GitHub history.

---

### 5.3 Access and Distribution
1. The `main` branch of the `redwitch.wiki` repository represents the official QMS documentation available to all employees.
2. Read access is provided to all users; write access is restricted to authorized maintainers.
3. Automated notifications (or release tags) may be used to announce new document versions.

---

### 5.4 Change Control
1. Revisions follow the **Pull Request Change Control Procedure (QP-08.05.06)**.
2. Each change must be linked to the relevant issue, CAR, or improvement request.
3. GitHub commit history and PR metadata serve as the official revision log.

---

### 5.5 Document Retention and Archiving
1. Superseded versions are retained in GitHub history (immutable).
2. If required, an archival branch (e.g., `archive/*`) or export to PDF may be used for long-term retention.
3. Retention period: minimum three (3) years or as required by regulation or contract.

---

### 5.6 External Documents
External standards, customer specifications, and supplier documents referenced by the QMS are maintained in read-only form with current-version verification at least annually.

---

### 5.7 Security and Authorization
1. Only authorized users with GitHub accounts and two-factor authentication may access controlled repositories.
2. Branch protection rules enforce review and approval before merge.
3. Access rights are reviewed annually by the Quality Manager.

---

### 5.8 Electronic Records and Signatures (21 CFR Part 11)
1. GitHub user authentication, audit logs, and immutable commit records satisfy the requirements of **§11.10(a–k)** for secure electronic records.
2. Reviewer approvals recorded in Pull Requests meet the intent of **§11.50** and **§11.70** for electronic signatures, as they:
   - Are linked to a unique user ID and verified login.
   - Capture the printed name (GitHub username), date/time, and meaning (approval).
   - Are permanently associated with the record and cannot be repudiated.
3. Users are responsible for maintaining the security of their GitHub credentials.

---

### 5.9 Periodic Review
1. Each controlled document shall be reviewed at least once every 24 months or as specified by the Process Owner.
2. Reviews are conducted through the same PR approval workflow and recorded in GitHub.

---

## 6. Records
| Record | Storage | Retention |
|--------|----------|-----------|
| Approved documents | GitHub `main` branch | Active |
| Superseded versions | GitHub history | ≥ 3 years |
| PR approval history | GitHub PR database | Permanent |
| Access control list | GitHub admin console | Annual review |

---

## 7. Roles and Responsibilities
| Role | Responsibility |
|------|----------------|
| **Document Author** | Drafts new or revised documents. |
| **Reviewer / Approver** | Verifies adequacy and approves via PR. |
| **Quality Manager** | Ensures control system integrity and compliance. |
| **System Administrator** | Maintains access controls and branch protections. |

---

**End of Procedure**
