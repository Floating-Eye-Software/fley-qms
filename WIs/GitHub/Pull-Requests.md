# **WI – GitHub Pull Request Procedure**

**WI Number:** WI-DOC-PR-001
**Title:** GitHub Pull Request Procedure
**Effective Date:** ____
**Owner:** Project Manager / Developer Lead

---

## **1. Purpose**

To implement **SOP-DOC-002 – Change & Version Control**, this WI defines the standardized process for creating, reviewing, and merging pull requests (PRs) in GitHub repositories to ensure:

* Code quality
* Traceability to requirements
* Compliance with the project Quality Plan

---

## **2. Scope**

Applies to all contributors working on any GitHub repository managed under FLEY’s QMS.

---

## **3. Procedure**

### **3.1 Pre-Requisites**

* Link your work to a **GitHub Issue** or documented requirement.
* Ensure local changes pass **unit tests and linters**.
* Update **documentation** if relevant (wiki, README, API docs).

---

### **3.2 Creating a Pull Request**

1. Create a feature or bugfix branch from `main` (naming convention: `feature/<short-description>` or `bugfix/<short-description>`).
2. Commit changes with clear messages referencing the related issue (e.g., `Fixes #42: corrected input validation`).
3. Push the branch to GitHub.
4. Open a pull request against the `main` branch.
5. Complete the PR template (if available), including:

   * Summary of changes
   * Related issue(s)
   * Testing performed
   * Impact analysis (dependencies, risks, documentation updates)

---

### **3.3 Review Process**

* At least **one reviewer** approval is required (two for high-risk or regulatory-impact changes).
* Reviewers check:

  * Code quality and adherence to coding standards
  * Test coverage and passing results
  * Traceability to requirements or design inputs
  * Security, privacy, and GDPR impact (if applicable)
* Reviewers may request changes; **merging is not allowed until approval is granted**.

---

### **3.4 Merging the Pull Request**

* Confirm that CI/CD pipelines pass (tests, lint, build).
* Merge using **Squash and Merge** (preferred for cleaner history).
* Delete the feature branch after merge.
* Tag the release if the change corresponds to a milestone or version increment.

---

### **3.5 Post-Merge Activities**

* Update linked issue(s) or milestone status.
* Update project board (e.g., move task from *In Progress* → *Done*).
* Update traceability matrix if requirements or design inputs were implemented or changed.

---

## **4. Recordkeeping**

* PRs, approvals, and CI/CD test results in GitHub serve as **official records**.
* Merge commit references issue/requirement → provides **traceability evidence**.
* Any exported reports or snapshots are stored in `/Records/` if required for regulatory or audit purposes.

---

## **5. Responsibilities**

| Role               | Responsibility                                                                 |
| ------------------ | ------------------------------------------------------------------------------ |
| Developer          | Create PRs, link to requirements/issues, respond to review feedback            |
| Reviewer(s)        | Conduct review, ensure compliance with SOP-DOC-002, approve or request changes |
| Project Maintainer | Ensure PRs meet quality requirements before merging                            |
