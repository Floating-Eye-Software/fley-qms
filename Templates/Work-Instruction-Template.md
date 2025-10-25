# **TPL - Work Instruction (WI) Template**

**Slug:** Work-Instruction-Template  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Document-Control-SOP   
**Controlled Source:** https://github.com/mlehotay/fley-qms/blob/main/Templates/Work-Instruction-Template.md  

---

## **1. Purpose**

Describe the purpose of this Work Instruction — what specific activity or task it defines within the broader process.

*Example:*

> “Describes the procedure for submitting, reviewing, and approving QMS document changes using GitHub Pull Requests.”

---

## **2. Scope**

Clarify the scope and applicability of this WI.

* **Applicability:** Identify the systems, repositories, departments, or teams where this WI applies.
* **Exclusions:** (Optional) Identify what is out of scope for this instruction.

---

## **3. References**

List related documents, standards, and references that support this WI.

* Related SOP: `SOP_[Process-Name]`
* Related WIs: [e.g., `WI_GitHub-Version-Control`, `WI_Template-Use`]
* ISO 9001:2015 — Clause 7.5: Documented Information
* [Other regulatory or process references as applicable]

---

## **4. Responsibilities and Authorities**

Define roles responsible for performing, reviewing, or verifying the activity described in this WI.

| Role                   | Responsibilities                                                                   | Authority / Decision Rights                             |
| ---------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------- |
| Operator / Technician  | Perform the steps in this Work Instruction as described.                           | Can execute the task; report issues to Supervisor/Lead. |
| Supervisor / Team Lead | Review and approve results, ensuring compliance with related SOPs.                 | Can approve task completion and escalate deviations.    |
| Process Owner          | Ensure the WI remains accurate and aligned with the SOP and current systems/tools. | Can request updates and approve minor revisions.        |
| Quality Manager / QA   | Ensure compliance with document control and quality requirements.                  | Can approve release and enforce corrective actions.     |

---

## **5. Step-by-Step Procedure**

Provide a detailed, sequential description of how to perform the task. Use clear, numbered steps and include code examples, screenshots, or command snippets as needed.

1. **Step 1:** [Describe the first action clearly.]
2. **Step 2:** [Describe the next step or decision.]
3. **Step 3:** [Add command examples, UI paths, or supporting visuals if helpful.]

```bash
# Example
git checkout -b change/<short-description>
git commit -m "Fixes #<IssueNumber> – Updated document"
git push origin change/<short-description>
```

4. **Step 4:** Submit a Pull Request (PR) for review.
5. **Step 5:** Reviewers approve and merge to `main`.
6. **Step 6:** Tag the approved commit (e.g., `WI_[Task-Name]_r2`).
7. **Step 7:** Publish the updated instruction or notify relevant users.

> **Tip:** Each step should produce a verifiable outcome or record (e.g., merged PR, updated tag, or published wiki page).

---

## **6. Records**

List any records, outputs, or evidence generated when executing this WI, and specify how they are controlled.

| Record / Artifact           | Responsible Owner            | Storage Location                 | Retention | Control Method              |
| --------------------------- | ---------------------------- | -------------------------------- | --------- | --------------------------- |
| Approved Work Instruction   | Document Control Coordinator | Controlled Source (wiki or repo) | Permanent | Revision control (Git tags) |
| Pull Requests / Commits     | Process Owner                | GitHub Repository                | Permanent | Git history                 |
| Related Issue or Change Log | Quality Manager              | Issue Tracker                    | Permanent | System record               |

> Controlled versions of this WI are maintained in GitHub.
> The `main` branch represents the current approved version.
> Approved revisions are identified by Git tags (e.g., `WI_[Task-Name]_r2`).
