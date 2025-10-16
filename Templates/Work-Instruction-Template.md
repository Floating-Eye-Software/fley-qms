# ✅ **Work Instruction (WI) Template**

# **WI – [Task / Activity Name]**

**Slug:** WI_[Task-Name]  
**Revision:** r#  
**Owner / Process Responsible:** [Role or Department]  
**Controlled Source:** https://github.com/<org>/<repo>/WIs/WI_[Task-Name].md  
**Related SOP:** SOP_[Process-Name]

---

## **1. Purpose**

Briefly describe what this WI instructs users to do.
Example: “Defines the steps for submitting and approving QMS document changes using GitHub Pull Requests.”

---

## **2. Scope**

* **Applicability:** Specify systems, repositories, or teams covered by this WI.
* **Exclusions:** Optional — identify what’s not covered.

---

## **3. References**

* Related SOP: [SOP_Document-Control]
* WI – GitHub Version Control and Traceability
* ISO 9001:2015, Clause 7.5

---

## **4. Responsibilities**

| Role   | Responsibilities                             |
| ------ | -------------------------------------------- |
| [Role] | Perform the steps described in this WI       |
| [Role] | Review and approve completion, if applicable |

---

## **5. Step-by-Step Procedure**

1. **Step 1:** [Describe first step]
2. **Step 2:** [Describe next step]
3. **Step 3:** [Add command examples or screenshots as needed]

```bash
# Example
git checkout -b change/<short-description>
git commit -m "Fixes #<IssueNumber> – Updated document"
git push origin change/<short-description>
```

4. **Step 4:** Submit a Pull Request for review.
5. **Step 5:** Reviewers approve and merge to `main`.
6. **Step 6:** Tag the approved commit (e.g., `WI_[Task-Name]_r2`).
7. **Step 7:** Publish or notify relevant users.

> Controlled versions of this WI are maintained in GitHub.
> The `main` branch represents the current approved version.
> Approved revisions are identified by Git tags.

---

## **6. Records / Documentation**

* All changes are traceable via Git commit history and Pull Requests.
* Approved versions are tagged in Git and accessible in the repository history.
* The `main` branch always reflects the current approved version.
