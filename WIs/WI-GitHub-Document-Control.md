# **Work Instruction – Document Control in GitHub**

**WI Number:** WI-DOC-001
**Related SOP:** SOP-DOC-001 – Document Control
**Effective Date:** ____
**Owner:** Quality Manager
**Review Cycle:** Annual

---

## **1. Purpose**

This WI defines the process for **creating, reviewing, approving, revising, distributing, and retiring controlled documents** in the FLEY GitHub wiki, ensuring compliance with:

* 21 CFR 820.40 (Document Controls)
* 21 CFR 820.30(j) (Design History File)
* ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 7.3.10

It also ensures traceability between documents, project milestones, issues, and evidence in GitHub.

---

## **2. Scope**

Applies to all FLEY controlled documentation, including SOPs, Work Instructions (WIs), Quality Plans, Templates, Project Docs, and Records.

---

## **3. Responsibilities**

| Role                          | Responsibility                                                                               |
| ----------------------------- | -------------------------------------------------------------------------------------------- |
| **Document Owner**            | Draft, maintain, and propose updates to controlled documents.                                |
| **Quality Manager**           | Review and approve all controlled documents. Ensure compliance with SOP-DOC-001.             |
| **Project Manager**           | Ensure project-level documents are maintained and linked to milestones/issues.               |
| **Developers / Team Members** | Reference controlled documents in issues, PRs, and CI/CD evidence. Follow approved SOPs/WIs. |

---

## **4. Step-by-Step Instructions**

### **4.1 Create a Controlled Document**

1. **Select the appropriate template** from `/Templates/` in the wiki (SOP, WI, Quality Plan).
2. **Create a new wiki page** under the correct folder:

   * SOPs → `/SOPs/`
   * WIs → `/WIs/`
   * Plans → `/Plans/`
   * Project Docs → `/Project-Docs/`
   * Records → `/Records/`
3. Assign a **Document Owner** in the header of the page.
4. Add a **Revision History table** and an empty **Linkage to Execution** section.

---

### **4.2 Drafting / Editing**

1. Draft your content in the wiki page or locally in markdown.
2. Reference **related issues, milestones, or project boards** in the “Linkage to Execution” section:

```markdown
## Linkage to Execution
- Milestones: [QMS Foundations](https://github.com/<org>/<repo>/milestone/1)
- Project Board: [Red Witch Kanban](https://github.com/<org>/<repo>/projects/1)
- Issues: [#42 Draft Design Control SOP](https://github.com/<org>/<repo>/issues/42)
```

3. Ensure all references are active links to maintain traceability.

---

### **4.3 Review & Approval via Pull Request (PR)**

1. Submit your wiki changes as a **Pull Request**.
2. Assign reviewers according to the document type:

   * SOP/WI/Plan → Quality Manager
   * Project Docs → Project Manager (plus QM if impacting QMS)
3. Include in the PR description:

   * Document purpose and scope
   * Milestones and issues linked as evidence
4. Reviewer(s) approve the PR; merge only after approval.
5. The merged version becomes the **controlled document**.

---

### **4.4 Updating / Revising a Document**

1. Update the document in the wiki via a new PR.
2. Increment **revision number** in the Revision History table:

   * Minor update → 0.1 → 0.2
   * Major update → 1.0 → 1.1
3. Update the **Linkage to Execution** section if milestones/issues change.
4. PR review and approval required.

---

### **4.5 Retiring / Obsoleting Documents**

1. Add `Obsolete` in the page title or heading.
2. Document reason for retirement and date.
3. Retired pages remain in **GitHub wiki history** for traceability.
4. Update any dependent documents or links to point to the current active version.

---

### **4.6 Linking to Evidence**

* Every controlled document should link to:

  * **Milestones** – to show plan execution
  * **Issues** – task-level execution, CAPA, audit items
  * **Project Boards** – Kanban view of ongoing/completed tasks
  * **CI/CD artifacts** – automated test reports, coverage, or build outputs

---

## **5. Records**

* Approved wiki page = controlled document
* GitHub PR = review & approval evidence
* GitHub issue references = task and evidence linkage
* Milestone completion = execution evidence
* CI/CD logs = verification evidence

---

## **6. References**

* SOP-DOC-001 – Document Control
* WI-GitHub-Project-Management
* 21 CFR 820.40, 820.30(j), 820.180
* ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 7.3.10

---

### ✅ **Tips / Best Practices**

1. Always update **Linkage to Execution** whenever project milestones/issues change.
2. Use **consistent naming conventions** for pages, PRs, and issues.
3. Keep prior versions in PR history — don’t delete old wiki pages.
4. Train team members to **link issues → PRs → CI/CD evidence** for complete traceability.
