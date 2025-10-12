# WI Template – [Task / Activity Name]

**WI ID:** [Unique ID, e.g., WI-001]
**Revision:** [r1, r2, etc.]
**Effective Date:** [YYYY-MM-DD]
**Owner / Process Responsible:** [Role or Department]
**Approved By:** [Role or Name]
**Controlled Source:** [GitHub Repository URL + file path]
**Approved Git Tag:** [e.g., WI-001_r1]

**Related SOP:** [SOP ID – Process Name]

---

## **1. Purpose**

Briefly describe the purpose of this Work Instruction.
Example: “Provides step-by-step instructions for submitting and approving changes to QMS documents using GitHub Pull Requests.”

---

## **2. Scope**

* **Applicability:** Specify the systems, repositories, documents, or teams this WI applies to.
* **Exclusions:** Optional — what is not covered by this WI.

---

## **3. Responsibilities**

| Role | Responsibilities |
|------|-----------------|
| [Role] | Perform the steps described in this WI |
| [Role] | Review and approve completion, if required |

---

## **4. Inputs**

| Input | Source | Notes |
|-------|--------|-------|
| [File, Form, Data] | [Location / System] | [Optional notes] |

---

## **5. Step-by-Step Procedure**

1. **Step 1:** [Description of the first step]
2. **Step 2:** [Description of the next step]
3. **Step 3:** [Include screenshots, Git commands, or code snippets if needed]

> Tip: Keep steps short and actionable. Use bullet points or numbered lists for clarity.

**Example (Git commands):**

```bash
# Create a feature branch
git checkout -b change/<short-description>

# Commit changes with meaningful message
git commit -m "Fixes #<IssueNumber> – Updated document"

# Push branch to remote
git push origin change/<short-description>
````

4. **Step 4:** Submit a Pull Request (PR) for review.
5. **Step 5:** Reviewers approve PR. Merge into `main`.
6. **Step 6:** Tag the approved commit with the revision (e.g., `WI-001_r2`).
7. **Step 7:** Update any dependent documentation or notify relevant teams.

---

## **6. Outputs / Results**

| Output                   | Destination / Usage          | Notes            |
| ------------------------ | ---------------------------- | ---------------- |
| [Document, File, Record] | [Repository, Folder, System] | [Optional notes] |

---

## **7. Records / Documentation**

* All changes are traceable via Git commit history and PRs.
* Approved versions are identified via Git tags.
* Optional export or archive: `[Location / ZIP / PDF]`.

---

## **8. References**

* Related SOP: [Documented Information Control SOP]
* WI – GitHub Pull Request and Branch Management
* WI – Git Version Control and Traceability
* ISO 9001:2015, Clause 7.5

---

## **9. Revision History**

| Revision | Date       | Description of Change | Author | Approved By |
| -------- | ---------- | --------------------- | ------ | ----------- |
| r1       | YYYY-MM-DD | Initial release       | [Name] | [Name]      |
| r2       | YYYY-MM-DD | [Describe update]     | [Name] | [Name]      |
