## **Work Instruction (WI): GitHub Repository and Wiki Management**

**Document Number:** [To be assigned]
**Effective Date:** [To be assigned]
**Revision:** [To be assigned]
**Related SOP:** Documented Information Control

---

### **1. Purpose**

To define how GitHub repositories, Wikis, and Issues are used to create, update, and control documented information required by the QMS, ensuring identification, availability, and protection in accordance with the Documented Information Control SOP.

---

### **2. Scope**

This WI applies to all QMS documents, procedures, work instructions, templates, and records maintained within GitHub repositories and Wikis.

---

### **3. Responsibilities**

| Role                                   | Responsibilities                                                                                           |
| -------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Process Owners**                     | Ensure controlled documents in their area are accurate, current, and approved.                             |
| **Document Control Coordinator (DCC)** | Maintain repository structure, branch protections, access permissions, and tag versions.                   |
| **All Employees**                      | Use the latest approved documents (from the `main` branch or GitHub Pages) and report any inconsistencies. |

---

### **4. Procedure**

#### **4.1 Creation and Updating**

1. **Document Creation**

   * New or revised documents are drafted in Markdown (`.md`), DOCX, or other approved formats in a feature branch.
   * Drafts must follow standard naming conventions (e.g., `SOP-001_DocumentedInformationControl.md`).
   * Each document includes:

     * Title and document number
     * Effective date and revision number
     * Version history table

2. **Review and Approval**

   * All proposed updates are submitted as a **Pull Request (PR)** for review (see Change Control WI).
   * Reviewers verify accuracy, formatting, and adequacy before merging.
   * The PR approval serves as the digital signature of reviewers and approvers.

3. **Identification and Metadata**

   * The Git commit history automatically tracks author, date, and change summary.
   * The document’s revision number must match the latest approved tag.

---

#### **4.2 Control of Documented Information**

1. **Availability and Access**

   * Approved documents are stored in the `main` branch.
   * GitHub’s default view and/or GitHub Pages publish the current controlled version.
   * Access is restricted via repository permissions:

     * **Read-only** for general users
     * **Write access** only for authorized editors
     * **Admin rights** reserved for the DCC or designated leads

2. **Storage and Preservation**

   * GitHub automatically maintains redundant copies and version history.
   * Regular repository backups may be exported to `.zip` archives and stored offline for contingency.

3. **Control of Changes**

   * All document modifications occur through Git commits and Pull Requests.
   * Branch protection prevents direct edits to `main`.
   * Git tags identify approved document revisions (e.g., `SOP-001_r1`, `WI-002_v3`).

4. **Retention and Disposition**

   * All past document versions are retained indefinitely within Git history.
   * Superseded documents may be archived in an `/archive` directory with a note in the header: “Obsolete – Superseded by [Tag].”

---

#### **4.3 External Documented Information**

* External standards (e.g., ISO 9001, regulations) are referenced via links in the Wiki.
* Controlled copies (e.g., PDFs or supplier docs) may be stored in a repository `/external` folder with restricted access.

---

#### **4.4 System Requirements for Electronic Control**

GitHub and associated workflows fulfill system control requirements:

| Requirement                          | GitHub Feature                                     |
| ------------------------------------ | -------------------------------------------------- |
| Authentication                       | Unique user logins via GitHub accounts or SSO      |
| Unauthorized modification prevention | Branch protection, required reviews                |
| Audit trails                         | Commit history and PR logs                         |
| Electronic signatures                | PR approvals traceable to authenticated users      |
| Backup and recovery                  | GitHub’s distributed redundancy + periodic exports |

---

#### **4.5 Records**

| Record Type                 | Location             | Retention                  |
| --------------------------- | -------------------- | -------------------------- |
| Repository commit history   | GitHub               | Permanent                  |
| Pull Requests and approvals | GitHub               | Permanent                  |
| Tagged document versions    | GitHub Releases      | Permanent                  |
| Archived files              | `/archive` directory | Permanent                  |
| Access logs                 | GitHub Admin Console | As per IT retention policy |

---

### **5. References**

* Documented Information Control SOP
* Change Control SOP
* Identification and Traceability SOP
* GitHub Documentation ([docs.github.com](https://docs.github.com))

---

### **6. Revision History**

| Revision | Date   | Description of Change | Approved By |
| -------- | ------ | --------------------- | ----------- |
| 0        | [Date] | Initial Release       | [Name]      |
