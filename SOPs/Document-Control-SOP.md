# **SOP – Document Control (FLEY)**

**SOP Number:** SOP-DOC-001
**Title:** Document Control
**Effective Date:** ____
**Owner:** Quality Manager
**Review Cycle:** Annual

---

## **1. Purpose**

This SOP establishes the requirements for creating, approving, revising, storing, distributing, and retiring controlled documents at Floating Eye Software (FLEY). It ensures compliance with:

* **21 CFR 820.40** – Document Controls
* **21 CFR 820.180** – Device History Record
* **ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 7.3.10** – Documented information, design & development file

The SOP ensures all QMS, project-level, and regulatory documents are **controlled, accessible, and traceable**.

---

## **2. Scope**

Applies to all FLEY controlled documents, including:

* Standard Operating Procedures (SOPs)
* Work Instructions (WIs)
* Quality Plans (org-level and project-level)
* Templates
* Project Requirements, Design Docs, Risk Analyses, Traceability Matrices
* Records (CAPA logs, audit logs, training records)

This SOP applies to all FLEY employees, contractors, and collaborators involved in QMS or product development activities.

---

## **3. Responsibilities**

| Role                                     | Responsibility                                                                                                |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Quality Manager / QMS Owner**          | Maintains SOP, approves all controlled documents, reviews changes.                                            |
| **Project Manager**                      | Ensures project-level documents follow this SOP; links issues and milestones to documentation.                |
| **Developers / Team Members**            | Use approved SOPs, WIs, and Plans; submit changes via PR; maintain traceability in issues and CI/CD evidence. |
| **Privacy Officer / Compliance Officer** | Ensures GDPR or regulatory content is current and referenced correctly.                                       |

---

## **4. Definitions**

* **Controlled Document:** Any document that defines processes, procedures, requirements, or specifications that must be followed and formally approved.
* **Uncontrolled Copy:** Any exported or printed version; must reference the controlled version in the wiki.
* **Document Owner:** Individual responsible for maintaining and approving a document.
* **Change Control:** Process to propose, review, approve, and implement revisions.

---

## **5. Document Lifecycle**

### **5.1 Creation**

1. Use approved **Templates** from `redwitch.wiki/Templates/`.
2. Assign a **Document Owner** (QM or Project Manager).
3. Create the new page in the appropriate wiki folder: `/SOPs/`, `/WIs/`, `/Plans/`, `/Project-Docs/`, `/Records/`.

### **5.2 Review & Approval**

1. Submit changes via **GitHub Pull Request** to the wiki.
2. Include references to related **issues, milestones, or project boards**.
3. At least one reviewer (QM or Project Manager) must approve.
4. Merge PR only after approval — merged version becomes the **controlled document**.

### **5.3 Revision**

1. Changes must include a **Revision History** table on the document page:

```markdown
| Rev | Date       | Author      | Change Description |
|-----|-----------|------------|------------------|
| 0.1 | 2025-09-25| M. Lehotay | Initial Draft     |
```

2. Update the **“Linkage to Execution”** section if milestone/issues references change.
3. Retain **prior versions** in the wiki history (GitHub versioning automatically tracks this).

### **5.4 Distribution**

* All controlled documents are **accessible via the wiki**.
* No uncontrolled copies are to be used for decision-making; printed/exported copies must reference the wiki link.

### **5.5 Obsolete / Retired Documents**

* Mark retired pages with `Obsolete` in the title or heading.
* Add reason for retirement and date.
* Maintain prior version in GitHub history for traceability.

---

## **6. Document Identification & Versioning**

* Document ID format: `SOP-XXX` for SOPs, `WI-XXX` for WIs, `PLAN-XXX` for Quality Plans.
* Use sequential **revision numbers** (0.1 → 1.0 → 1.1) for minor and major changes.
* Include **effective date** and **review cycle** on the document header.

---

## **7. Document Access & Control**

* **Wiki is the single source of truth**.
* Links to GitHub Issues / Milestones / Project Boards provide evidence of execution.
* Use **PR approvals** as formal review record.
* Version history in GitHub ensures traceability.

---

## **8. Record of Changes / Revision History**

* Maintain a **Revision History** table at the top of every document.
* All prior versions are preserved via **GitHub wiki history**.

---

## **9. References**

* 21 CFR 820.40 – Document Controls
* 21 CFR 820.180 – Device History Record
* 21 CFR 820.30(j) – Design History File
* ISO 13485:2016 – Clauses 4.2, 4.2.3, 4.2.4, 7.3.10
* SOP-Quality-Planning
* WI-GitHub-Project-Management

---

## **10. Appendices**

* **Appendix A – GitHub Integration:**

  * All document PRs must reference the governing **milestones** and **issues**.
  * The “Linkage to Execution” section in each wiki page shows the related milestones, project boards, and issues.
  * CI/CD and automated test reports are linked from the Records pages.
