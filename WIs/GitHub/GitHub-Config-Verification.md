---
slug: GitHub-Config-Verification
revision: r1
type: WI
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-Config-Verification.md
---

# **WI – GitHub Configuration Verification**

## **1. Purpose**

To define a controlled method for verifying GitHub repository configurations intended for QMS-controlled operations. This Work Instruction ensures that settings, workflows, and templates are functionally equivalent between **test-repo** (uncontrolled) and **fley-qms** (production) prior to implementing changes in a controlled repository.

> **Note on Validation:**
> Verification of individual configuration changes is performed using test-repo.
> This WI governs verification only; it does not determine whether the QMS configuration is fit for purpose (validation).
> **Full validation of the complete FLEY QMS will occur once, at the conclusion of the “QMS Foundations” milestone**, after all core workflows, records, and operational procedures have been implemented.

---

## **2. Scope**

Applies to all repositories used for QMS operations where configuration behavior impacts document control, workflow, or record integrity, including:

* Repository settings (branch protections, merge strategies, required reviewers)
* Issue and Pull Request templates
* Labels and workflow metadata
* GitHub Actions or automated workflows

**Exclusions:**

* No QMS-controlled content or records are stored in test-repo.
* Evidence such as screenshots, attachments, or historical commits are **not** preserved in test-repo.

---

## **3. References**

* Change-Control-SOP
* Document-Control-SOP
* GitHub–Change–Control
* GitHub–QMS–Operations
* FLEY-Planning-Workflow (formerly FLEY-Action-Management)

---

## **4. Responsibilities**

| Role                                 | Responsibilities                                                                                     |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| **QMS Administrator**                | Establishes test-repo equivalency; ensures proper configuration replication; documents verification. |
| **Process Owner / Change Requestor** | Identifies required configuration changes; performs verification steps.                              |
| **Reviewer / Approver**              | Reviews verification outcomes and approves configuration changes.                                    |
| **Quality Manager**                  | Confirms adherence to configuration verification requirements and maintains oversight.               |

---

## **5. Procedure**

### **5.1 Prepare Test Repository**

1. Ensure test-repo is reset or aligned to a clean baseline.
2. Confirm appropriate administrative access.
3. Verify that baseline configuration matches production for the items being tested.

---

### **5.2 Define Configuration Scope**

Identify which configuration elements must match `fley-qms`, including:

* Branch protection rules
* CODEOWNERS and required reviewers
* Issue and PR templates
* Labels and metadata
* Repository settings affecting workflow routing
* GitHub Actions or automations (if applicable)

---

### **5.3 Establish Equivalency**

1. Replicate configuration items from `fley-qms` into test-repo.
2. Confirm that the relevant settings match.
3. Document equivalency confirmation within the related Issue in fley-qms.

> **test-repo is uncontrolled** – it may be reset, overwritten, or deleted at any time.

---

### **5.4 Implement and Test Configuration Changes**

1. Make configuration changes directly in test-repo.
2. Create dummy Issues or PRs where needed to test behavior.
3. Verify that templates render as expected and labels apply correctly.
4. Confirm that workflow behavior (branch protection, review rules, automation behavior) matches expectations.
5. Capture simple screenshots or notes as **verification evidence** attached to the CR Issue in `fley-qms`.
6. Evidence must show at least one successful render of each affected template, label set, or workflow item.

---

### **5.5 Apply Verified Changes to Production (fley-qms)**

1. Open or update a Change Request (CR) Issue in `fley-qms`.
2. Create an implementation branch.
3. Apply the verified configuration changes.
4. Submit a Pull Request to merge into `main`.
5. Reviewers confirm the change behaves as intended.
6. Merge the PR - this is the formal approval event.

---

### **5.6 Records and Traceability**

* Verification evidence is attached to the CR Issue in `fley-qms`.
* PRs, commits, and configuration updates are retained as controlled records.
* test-repo Issues and attachments are for internal reference only and are not controlled records.

---

## **6. Records**

| Record Type           | Description                                           | Location              | Retention            |
| --------------------- | ----------------------------------------------------- | --------------------- | -------------------- |
| Verification Evidence | Screenshots / notes supporting configuration behavior | CR Issue (`fley-qms`) | Indefinite           |
| CR Issue              | Change request                                        | fley-qms              | Indefinite           |
| PR                    | Review and approval                                   | fley-qms              | Indefinite           |
| Commits / Tags        | Controlled configuration                              | fley-qms              | Indefinite           |
| test-repo Issues      | Internal reference only                               | test-repo             | May be deleted/reset |
