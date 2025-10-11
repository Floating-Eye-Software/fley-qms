## 🧭 **Work Instruction (WI): GitHub Document Control**

**Document Number:** WI-004
**Effective Date:** 2025-10-11
**Revision:** r1
**Related SOP:** Document Control SOP
**Controlled Source:** [GitHub Repository URL]

---

### **1. Purpose**

To define how controlled QMS documents are created, numbered, revised, and maintained within GitHub, ensuring unique identification, revision tracking, and control of approved versions.

---

### **2. Scope**

Applies to all QMS documents and controlled files managed in GitHub, including Standard Operating Procedures (SOPs), Work Instructions (WIs), Policies (POLs), Templates (TPLs), and Records (REC).

---

### **3. Responsibilities**

| Role                         | Responsibilities                                                               |
| ---------------------------- | ------------------------------------------------------------------------------ |
| **Authors / Process Owners** | Create and maintain documents according to numbering and metadata standards.   |
| **Reviewers / Approvers**    | Review Pull Requests and approve document changes in GitHub.                   |
| **Quality Manager / CCC**    | Verify correct numbering, tagging, and repository organization.                |
| **All Users**                | Access and use only approved versions from the main branch or tagged releases. |

---

### **4. Procedure**

#### **4.1 Document Numbering**

1. Document numbers follow the format:

   ```
   [PREFIX]-[###]_[Title].md
   ```

   Example: `SOP-003_Document-Control.md`

2. Prefix conventions:

   | Type                         | Prefix |
   | ---------------------------- | ------ |
   | Standard Operating Procedure | SOP    |
   | Work Instruction             | WI     |
   | Template                     | TPL    |
   | Policy                       | POL    |
   | Record                       | REC    |

3. Sequential numbering is assigned manually by the author, verified by the reviewer to ensure uniqueness.

---

#### **4.2 File Header Metadata**

Each controlled document must include the following Markdown header at the top of the file:

```markdown
# SOP-003 – Document Control
**Revision:** r1  
**Effective Date:** 2025-10-11  
**Approved By:** [Name / Title]  
**Controlled Source:** https://github.com/[org]/[repo]/SOPs/SOP-003_Document-Control.md
```

Optional fields (e.g., “Supersedes” or “Obsolete Date”) may be added if applicable.

---

#### **4.3 Creating and Tagging Approved Versions**

1. All document updates are submitted via a **Pull Request (PR)**.

2. After review and approval, the PR is merged into the `main` branch.

3. Create a Git tag to mark the approved revision:

   ```bash
   git tag SOP-003_r2
   git push origin SOP-003_r2
   ```

4. The tag name must match the document identifier and revision number.

5. The tag and corresponding commit serve as the **official record** of approval and revision.

---

#### **4.4 Locating the Next Available Document Number**

1. Review the `/SOPs`, `/WIs`, or applicable folder to determine the next sequential number.
2. Search for existing filenames using:

   ```bash
   ls SOP-* | sort
   ```
3. Assign the next number in sequence.

---

#### **4.5 Managing Obsolete or Superseded Documents**

1. When a document is replaced:

   * Update the header to indicate **OBSOLETE** and include the superseding document number.
   * Optionally move the file to `/archive/`.
2. The previous tag remains in Git as a permanent record.

---

#### **4.6 Viewing Revision History**

To view all revisions and authors for a document:

```bash
git log --follow --pretty=format:"%h %ad %an %s" --date=iso path/to/SOP-003_Document-Control.md
```

This provides the traceability record required by ISO 9001 Clause 7.5.

---

### **5. Records and Retention**

| Record Type    | Location          | Retention  |
| -------------- | ----------------- | ---------- |
| Document files | GitHub repository | Indefinite |
| Git tags       | GitHub            | Indefinite |
| Pull Requests  | GitHub            | Indefinite |
| Commit history | Git repository    | Indefinite |

---

### **6. References**

* SOP – Document Control
* SOP – Change Control
* SOP – Identification and Traceability
* WI – GitHub Pull Request & Branch Management
* WI – Git Version Control and Traceability
* ISO 9001:2015, Clauses 7.5.2 and 7.5.3

---

### **7. Revision History**

| Revision | Date       | Description of Change                                                         | Approved By |
| -------- | ---------- | ----------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release implementing Git-based document numbering and revision system | [Name]      |
