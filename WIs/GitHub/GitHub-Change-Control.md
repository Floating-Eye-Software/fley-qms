---
slug: GitHub-Change-Control
revision: r3
type: WI
status: approved
effective: 2025-12-04
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

---

### **5.2 Create a Change Branch**

Create a new **branch** from the protected `main` branch:

```bash
git checkout main
git pull
git checkout -b change/42-update-change-control
```

---

### **5.3 Implement the Change**

Implement and test changes as needed.

Commit to the change branch with a descriptive message referencing the Issue number:

```bash
git commit -m "Fixes #42 – Updated document identification process"
```

Each commit referencing an Issue provides traceability and establishes a record of implementation activity.

---

### **5.3.1 Selectively Restoring Files From Another Branch**

If needed changes exist on another branch (e.g., `dev`) but **other commits on that branch must not be included**, use Git’s selective restore capability:

1. Ensure you are on the change branch created from `main`:

   ```bash
   git checkout change/42-update-change-control
   ```

2. Restore only the specific files from the source branch:

   ```bash
   git restore --source dev -- path/to/file.md
   ```

3. Stage and commit the restored file(s):

   ```bash
   git add path/to/file.md
   git commit -m "Fixes #42 – Restored file changes from dev (selectively)"
   ```

This method ensures:

* No unrelated commits from the source branch are introduced
* Only intended file changes appear in the PR
* The resulting PR diff is clean, minimal, and audit-friendly

---

### **5.4 Open a Pull Request**

Open a **Pull Request (PR)** to merge the change branch into `main`.

The PR description must include:

* A link to the related Issue, e.g., `Fixes #42`
* A concise summary of the proposed changes
* Any relevant testing, verification, or validation notes

The PR serves as the **formal review and approval record**.

---

### **5.5 Review and Approval**

All PRs must be reviewed for:

* Correctness and completeness
* Compliance with applicable WIs, SOPs, and templates
* Proper metadata and revision control
* Alignment with the originating CR Issue

Reviewers use GitHub’s review tools (**Approve**, **Comment**, **Request changes**). Required reviewers are defined in `CODEOWNERS`.

GitHub review actions and comments constitute **electronic signatures** under 21 CFR Part 11 and ISO 13485 §4.2.4.

#### **5.5.1 Standard Workflow (Multiple Reviewers)**

* Reviewers use the **“Approve”** action.
* GitHub automatically records identity and timestamp.

#### **5.5.2 Single-Approver Workflow**

When the PR author is also the sole reviewer, GitHub disables “Approve.”

To remain compliant:

1. Add a PR comment containing:

   **“Approved”** or **“PR Approved.”**

2. This comment + GitHub metadata constitutes the electronic approval.

---

### **5.6 Finalize Metadata Before Merge**

Immediately prior to merging the Pull Request, the **QMS Approver** updates the YAML metadata for each modified controlled document.

All controlled documents remain in **status: draft** while on the change branch.
The **Approver**, not the Author, performs the final metadata update.

Update the following fields per *GitHub-Document-Control*:

```yaml
revision: r#
status: approved
effective: YYYY-MM-DD   # date of intended merge
```

Steps:

1. Check out the PR branch.
2. Update metadata fields in all controlled documents.
3. Commit metadata updates to the same branch:

```bash
git add .
git commit -m "Finalize approval metadata (CR #42)"
git push
```

4. Confirm the PR reflects the final metadata.

The Approver then proceeds to the merge as the formal release event.

---

### **5.7 Merge and Release**

The **CCC** verifies:

* CR linkage
* Required approvals
* Correct metadata (`revision`, `status: approved`, `effective:` date)
* All status checks passed (if configured)

The Pull Request is then merged into `main`.

**Merge constitutes formal release approval**, and the merge commit becomes the authoritative, controlled version of all included documents.

---

### **5.8 Create the Record Tag**

After merge, create a Record Tag for each controlled document updated:

```bash
git tag GitHub-Change-Control_r2
git push origin GitHub-Change-Control_r2
```

Tags:

* Must match slug + revision
* Are immutable
* Represent the effective revision
* `main` always reflects the current approved version

The PR, merge commit, and tag together form the complete approval and effective-date record.

---

### **5.9 Close-Out**

* Confirm the CR Issue is closed
* Verify tags exist
* Confirm branch protection rules were applied
* Update boards or logs as required

---

### **5.10 Branch and Access Control**

1. **Protect** the `main` branch:

   * Require PR reviews
   * Disallow direct commits
   * Disallow force pushes
   * Require passing status checks (if configured)

2. **Naming conventions** promote clarity:

   ```
   fix/translation-accuracy
   change/update-decision-matrix
   feature/new-qms-template
   objective/establish-metrics
   ```

3. After merge, local branches may be deleted. Remote branches may be deleted or retained per organizational practice. All history remains traceable through Git and the closed PR.

---

### **5.11 Handling Unauthorized Changes**

1. Open a **CAPA Issue** for any unapproved changes.

2. Revert unauthorized commits via new PR:

   ```bash
   git revert <commit-hash>
   ```

3. Merge the corrective PR and create a new tag for the corrected revision.

4. Close the CAPA once corrective actions are verified.

---

## **6. Records**

| Record Type             | Description                                                | Location            | Retention  |
| ----------------------- | ---------------------------------------------------------- | ------------------- | ---------- |
| GitHub Issues           | CRs, CAPAs, and related records                            | GitHub              | Indefinite |
| Pull Requests           | Review, approval, and merge record (electronic signatures) | GitHub              | Indefinite |
| Commits                 | Implementation history and traceability                    | Git repository      | Indefinite |
| Tags                    | Approved effective revision identifiers                    | GitHub              | Indefinite |
| Branch Protection Rules | Configuration of repository controls                       | Repository Settings | Indefinite |
