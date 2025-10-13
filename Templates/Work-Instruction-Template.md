# WI – [Task / Activity Name]

**Slug:** WI_[Task-Name]  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Owner / Process Responsible:** [Role or Department]  
**Approved By:** [Role or Name]  
**Controlled Source:** https://github.com/[org]/[repo]/WIs/WI_[Task-Name].md  
**Related SOP:** SOP_[Process-Name]

---

## **1. Purpose**

Briefly describe the purpose of this Work Instruction.  
Example: “Provides step-by-step instructions for submitting and approving QMS document changes via GitHub Pull Requests.”

---

## **2. Scope**

* **Applicability:** Specify the systems, repositories, or teams this WI applies to.  
* **Exclusions:** Optional — identify activities not covered by this WI.

---

## **3. References**

* Related SOP: [SOP_Document-Control]  
* WI – GitHub Pull Request Workflow  
* WI – Git Version Control and Traceability  
* ISO 9001:2015, Clause 7.5  

---

## **4. Responsibilities**

| Role | Responsibilities |
|------|------------------|
| [Role] | Perform the steps described in this WI |
| [Role] | Review and approve completion, if required |

---

## **5. Inputs**

| Input | Source | Notes |
|-------|--------|-------|
| [File, Form, Data] | [Location / System] | [Optional notes] |

---

## **6. Step-by-Step Procedure**

1. **Step 1:** [Description of the first step]  
2. **Step 2:** [Description of the next step]  
3. **Step 3:** [Include screenshots, Git commands, or code snippets as needed]  

```bash
# Example (Git commands)
git checkout -b change/<short-description>
git commit -m "Fixes #<IssueNumber> – Updated document"
git push origin change/<short-description>
````

4. **Step 4:** Submit a Pull Request (PR) for review.
5. **Step 5:** Reviewers approve PR and merge to `main`.
6. **Step 6:** Tag the approved commit with the revision (e.g., `WI_[Task-Name]_r2`).
7. **Step 7:** Notify relevant teams or update dependent documentation.

> **Tip:** Keep steps short and actionable. Use bullets or numbered lists for clarity.

---

## **7. Outputs / Results**

| Output                   | Destination / Usage          | Notes            |
| ------------------------ | ---------------------------- | ---------------- |
| [Document, File, Record] | [Repository, Folder, System] | [Optional notes] |

---

## **8. Records / Documentation**

* All changes are traceable via Git commit history and Pull Requests.
* Approved versions are identified via Git tags.
* The `main` branch represents the current approved version.
