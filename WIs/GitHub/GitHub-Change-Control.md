---
slug: GitHub-Change-Control
revision: r2
type: WI
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-Change-Control.md
---

# **WI – GitHub Change Control**

## **1. Purpose**

To define the standardized method for proposing, reviewing, approving, and implementing changes to QMS-controlled documents and configurations using GitHub Issues, branches, and Pull Requests (PRs).

This Work Instruction implements the Change Control SOP within a Git-based environment.

---

## **2. Scope**

This WI applies to all repositories containing QMS-controlled documentation or configuration data managed in GitHub, including Standard Operating Procedures (SOPs), Work Instructions (WIs), Templates (TPLs), and Records (RECs).

---

## **3. References**

* SOP – Change Control
* SOP – Document Control
* WI – GitHub–Document-Control
* WI – GitHub–QMS–Setup
* TPL-GH-Change-Request template
* TPL-GH-Pull-Request template
* ISO 9001:2015 §§6.3, 7.5.3
* 21 CFR Part 11

---

## **4. Responsibilities**

| Role                                 | Responsibilities                                                                          |
| ------------------------------------ | ----------------------------------------------------------------------------------------- |
| **Change Requestor (Author)**        | Initiates the change through a GitHub Issue and implements updates in a dedicated branch. |
| **Reviewer / Approver**              | Reviews and approves PRs for completeness, accuracy, and compliance before merge.         |
| **Change Control Coordinator (CCC)** | Verifies correct Issue linkage, approvals, and tags before merging.                       |
| **Quality Manager**                  | Ensures adherence to the change control process and maintains record integrity in GitHub. |

---

## **5. Procedure**

### **5.1 Create a Change Request Issue**

Begin every controlled change with a CR Issue using the approved template.

Required fields include:

* Purpose and justification for change
* Impact and risk assessment
* References to affected SOPs, WIs, or CAPAs

The Issue ID becomes the CR identifier.

### **5.2 Create a Change Branch**

Create a new **branch** from the protected `main` branch:

```bash
git checkout -b change/42-update-change-control
```

### **5.3 Implement the Change**

Implement and test changes as needed.

Commit to the change branch with a descriptive message referencing the Issue number:

```bash
git commit -m "Fixes #42 – Updated document identification process"
```

> Each commit referencing an Issue provides traceability and establishes a record of implementation activity.

---

### **5.4 Open a Pull Request**

Open a **Pull Request (PR)** to merge the change branch into `main`.

The PR description must include:

* A link to the related Issue (CR), e.g. `Fixes #42`
* A concise summary of the proposed changes
* Any relevant testing, verification, or validation notes

The PR serves as the **formal review and approval record** for the change.

---

### **5.5 Review and Approval**

Reviewers evaluate the PR for:
* Correctness and completeness
* Compliance with applicable WIs, SOPs, and templates
* Proper metadata and revision control
* Alignment with the CR Issue scope

Reviewers provide comments or approvals directly in GitHub using the review tools:

* **Approve**
* **Comment**
* **Request changes**

Required reviewers are designated in the repository’s `CODEOWNERS` file.

GitHub approval actions constitute **electronic signatures** under 21 CFR Part 11 and ISO 13485 §4.2.4.

Once all required approvals are complete, the PR is ready for merge.

---

### **5.6 Finalize Metadata Before Merge**

Before merge, update each controlled file’s header per GitHub-Document-Control, including:

```yaml
revision: r#
status: approved
effective: YYYY-MM-DD
```

Commit metadata updates to the same branch:

```bash
git add .
git commit -m "Finalize approval metadata (CR #42)"
git push
```

---

### **5.7 Merge and Release**

CCC verifies:

* Proper CR linkage
* Required approvals
* Metadata correctness
* All checks passed

Then merges via PR.

Merge constitutes **formal release approval**.

---

### **5.8 Create the Record Tag**

After merge, create the Record Tag(s) for each controlled document updated.

```bash
git tag GitHub-Change-Control_r2
git push origin GitHub-Change-Control_r2
```

Tags:

* Must match slug + revision
* Are immutable
* Represent the effective revision
* `main` always reflects the current approved version

> The PR, merge commit, and associated tag together form the complete electronic approval and effective-date record.

---

### **5.9 Close-Out**

* Verify the CR Issue is closed
* Verify tags appear in the repository
* Confirm branch protection rules were followed
* Update boards or logs as required

---

### **5.10 Branch and Access Control**

1. The `main` branch must be **protected** to ensure data integrity:

   * Require PR reviews before merging
   * Disallow direct commits
   * Disallow force pushes and branch deletions
   * Require passing status checks (if configured)

2. Branch naming conventions promote traceability:

   ```
   fix/translation-accuracy
   change/update-decision-matrix
   feature/new-qms-template
   objective/establish-metrics
   ```

3. After merge, local branches may be deleted to maintain repository hygiene. Remote branches are retained indefinitely for traceability. All history remains traceable in Git logs and the closed PR.

---

### **5.11 Handling Unauthorized Changes**

1. If an unapproved or incorrect change is discovered in `main`:

   * Immediately open a **CAPA Issue** referencing the affected commit or PR.
   * Document the event, impact, and corrective action.

2. Revert the unauthorized change using a new PR that references the CAPA:

   ```bash
   git revert <commit-hash>
   ```

3. After verification and approval, merge the corrective PR and create a new tag (e.g., `_r3`).

4. Close the CAPA when corrective actions are verified as effective.

---

## **6. Records**

| Record Type             | Description                                                | Location            | Retention  |
| ----------------------- | ---------------------------------------------------------- | ------------------- | ---------- |
| GitHub Issues           | Change Requests (CRs), CAPAs, and related records          | GitHub              | Indefinite |
| Pull Requests           | Review, approval, and merge record (electronic signatures) | GitHub              | Indefinite |
| Commits                 | Implementation history and traceability                    | Git repository      | Indefinite |
| Tags                    | Approved and effective revision identifiers                | GitHub              | Indefinite |
| Branch Protection Rules | Configuration record of repository controls                | Repository Settings | Indefinite |

> All GitHub metadata and configuration serve as the official QMS record of change control and approval.
