
# **Pull Request Procedure**

## **1. Purpose**

This procedure defines the standardized process for creating, reviewing, and merging pull requests (PRs) to ensure code quality, traceability to requirements, and compliance with the Software Development Plan (SDP) and Quality Plan.

---

## **2. Scope**

This procedure applies to all contributors working on the Red Witch project repository.

---

## **3. Procedure**

### **3.1 Pre-Requisites**

* Ensure the work is linked to a **GitHub Issue** or **requirement**.
* Ensure local changes pass all **unit tests and linters**.
* Write/update **documentation** if relevant (wiki, README, or API docs).

---

### **3.2 Creating a Pull Request**

1. Create a feature branch from `main` (naming convention: `feature/<short-description>` or `bugfix/<short-description>`).
2. Commit changes with clear messages referencing the related issue (e.g., `Fixes #42: corrected input validation`).
3. Push the branch to GitHub.
4. Open a pull request against the `main` branch.
5. Fill in the **PR template** (if available), including:

   * Summary of changes
   * Related issue(s)
   * Testing performed
   * Impact analysis (e.g., dependencies, risks, documentation updates)

---

### **3.3 Review Process**

* At least **one reviewer** (preferably two for high-risk changes) must approve the PR.
* Reviewers check:

  * Code quality and adherence to coding standards
  * Test coverage and passing test results
  * Traceability to requirements / design inputs
  * Security, privacy, and GDPR impact (if applicable)
* Reviewers may request changes before approval.

---

### **3.4 Merging the Pull Request**

* Once approved:

  * Ensure CI/CD pipeline passes (tests, lint, build).
  * Merge using **Squash and Merge** (preferred) to keep commit history clean.
  * Delete the feature branch after merge.

* Tag the release if the change corresponds to a milestone or version increment.

---

### **3.5 Post-Merge Activities**

* Ensure linked issue(s) are automatically closed or updated.
* Update project board (e.g., move task from *In Progress* → *Done*).
* If applicable, update **traceability matrix** with new/changed requirement → implementation → test links.

---

## **4. Recordkeeping**

* PRs and reviews are stored permanently in GitHub and serve as official records.
* CI/CD test reports are linked to each PR and retained as evidence.

---

## **5. Responsibilities**

* **Developer:** Create PRs, ensure traceability, respond to review feedback.
* **Reviewer(s):** Conduct reviews, ensure compliance with SOPs, approve or request changes.
* **Project Maintainer:** Ensure PRs meet quality requirements before merging.
