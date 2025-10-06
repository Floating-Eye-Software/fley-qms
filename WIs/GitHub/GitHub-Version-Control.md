## **Work Instruction (WI): Git Version Control and Traceability**

**Document Number:** [To be assigned]
**Effective Date:** [To be assigned]
**Revision:** [To be assigned]
**Related SOP:** Identification and Traceability SOP

---

### **1. Purpose**

To define how Git and GitHub are used to identify, version, and trace all controlled outputs (documents, software, and records) throughout their lifecycle, ensuring conformity and maintaining continuous traceability.

---

### **2. Scope**

This Work Instruction applies to all repositories, documents, and controlled files managed in GitHub that fall under the scope of the Identification and Traceability SOP, including QMS documentation, configuration files, and software components.

---

### **3. Responsibilities**

| Role                        | Responsibilities                                                                                                                  |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Process Owners**          | Ensure repositories and branches are maintained in accordance with this WI.                                                       |
| **Quality Assurance (QA)**  | Verify that identification, versioning, and traceability mechanisms are implemented and records are retained.                     |
| **Contributors/Developers** | Follow the identification and traceability practices outlined in this WI when committing, branching, tagging, or merging content. |

---

### **4. Definitions**

| Term             | Definition                                                                                                  |
| ---------------- | ----------------------------------------------------------------------------------------------------------- |
| **Commit**       | A recorded change in Git, including author, date, description, and unique hash identifier.                  |
| **Branch**       | A logical line of development used to separate approved (main) from draft or in-progress changes.           |
| **Tag**          | A permanent marker in Git identifying an approved or released version.                                      |
| **HEAD**         | The latest commit on the current branch. The `HEAD` of `main` represents the current approved version.      |
| **GitHub Pages** | A hosted website automatically generated from the approved repository branch to publish controlled content. |

---

### **5. Procedure**

#### **5.1 Identification**

1. All controlled outputs (documents, files, or components) shall reside in a GitHub repository with a clear and descriptive directory structure.

   * Example:

     ```
     /SOPs/
     /WIs/
     /Templates/
     ```
2. Each output is uniquely identified by:

   * Repository name
   * File path and filename
   * Commit hash (e.g., `8f2e3b7`)
   * Branch name (e.g., `main`, `feature/change-control`)
   * Tag (for approved/released versions, e.g., `v1.0` or `SOP-001_r2`)
3. The status of each document or output is determined by its branch:

   * `main`: Approved and controlled content
   * `draft` or `feature/*`: In review or development
   * `archive`: Superseded or obsolete material

---

#### **5.2 Traceability**

1. Each commit must include:

   * A **meaningful commit message** describing the change
   * The **author** and **date** automatically recorded by Git
   * Links to relevant Issues or Pull Requests for context (e.g., `Fixes #45`)
2. Commit history shall provide a complete record of changes, including what changed, when, and by whom.
3. Pull Requests (PRs) must be used for all changes to controlled branches.

   * PR discussion threads serve as approval and review records.
   * Merging a PR indicates formal approval under the Change Control SOP.
4. Tags shall be created to mark major or approved versions of documents or products.

   * Tag naming convention: `[DocumentID]_r[Revision]` or `[ProjectName]_v[Version]`
   * Example: `SOP-001_r2` or `QMS-v1.3`

---

#### **5.3 Version Control and Publication**

1. The **HEAD of the `main` branch** represents the current, approved version of the output.
2. GitHub’s default branch setting ensures users always see the approved version by default.
3. Optionally, **GitHub Pages** may be used to publish the approved content:

   * Configured to deploy from the `main` (or `gh-pages`) branch only.
   * Provides a read-only, web-accessible version of controlled documents.
   * Automatically updates after approved merges.

---

#### **5.4 Handling Changes**

1. All changes must be proposed via a new branch and Pull Request.
2. Reviewers verify traceability to change requests or CAPAs before merging.
3. Once approved and merged into `main`, the previous tag is archived and a new tag is created to reflect the updated version.
4. The commit history and tags together form the permanent traceability record.

---

#### **5.5 Records**

The following serve as official identification and traceability records:

| Record Type          | Source                  | Retention                |
| -------------------- | ----------------------- | ------------------------ |
| Commit logs          | Git repository          | Permanent                |
| Pull Request history | GitHub repository       | Permanent                |
| Tags and releases    | GitHub repository       | Permanent                |
| GitHub Pages site    | Automatically generated | Current approved version |
| Linked Issues        | GitHub repository       | Permanent                |

All records are stored in GitHub, which maintains automatic timestamps, authorship, and version history.

---

### **6. References**

* Identification and Traceability SOP
* Document Control SOP
* Change Control SOP
* ISO 9001:2015, Clauses 7.5 and 8.5.2
* GitHub Documentation: [https://docs.github.com](https://docs.github.com)

---

### **7. Revision History**

| Revision | Date   | Description of Change | Approved By |
| -------- | ------ | --------------------- | ----------- |
| 0        | [Date] | Initial Release       | [Name]      |
