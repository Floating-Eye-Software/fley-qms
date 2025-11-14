---
slug: GitHub-Document-Control
revision: r2
type: WI
status: approved
effective: 2025-11-14
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-Document-Control.md  
---

# **WI – GitHub Document Control**

## **1. Purpose**

To define the method for creating, revising, approving, and maintaining controlled QMS documents within GitHub, in alignment with the Document Control SOP.
This Work Instruction (WI) specifies how GitHub’s native version control, pull request, and tagging functions fulfill document control requirements.

---

## **2. Scope**

This WI applies to all controlled QMS documents maintained in the GitHub repository, including SOPs, WIs, Templates (TPLs), and controlled Records (RECs).
It describes *how* document control is implemented within GitHub. The SOP defines *what* must be achieved.

---

## **3. References**

* SOP – Document Control
* WI – GitHub–QMS–Setup
* TPL – Standard-Operating-Procedure-Template
* TPL – Work-Instruction-Template
* TPL – Header-Template
* ISO 9001:2015 §§7.5.2–7.5.3
* 21 CFR Part 11

---

## **4. Responsibilities**

| Role                            | Responsibilities                                                                                                  |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Authors / Process Owners**    | Draft and maintain controlled documents using the correct slug and revision formatting.                           |
| **Reviewers / Approvers**       | Review proposed changes in Pull Requests (PRs) and provide formal approval comments.                              |
| **Quality Manager / DCC / CCC** | Verify correct structure, header format, and tagging. Ensure only approved content appears at the HEAD of `main`. |
| **All Users**                   | Use only the approved versions visible in the wiki or `main` branch.                                              |

---

## **5. Procedure**

### **5.1 Document Identification and Naming**

1. Each controlled document resides in the appropriate folder (`/SOPs`, `/WIs`, `/Templates`, `/Records`, `/External/`, etc.).
2. Every document must have a **unique slug** that identifies it within the QMS.
3. Document type is indicated in the header (`type` field) and may be any of: SOP, WI, TPL, REC, CFG, MAP, PLAN, EXT, or others.
4. Type codes may appear in the filename but are **not required**.
5. Each document or metadata file must be versioned and traceable through Git commits and tags.
6. Superseded revisions remain accessible via tags; only the latest approved revision is present on `main`.

| Type                         | Code | Example                          |
| ---------------------------- | ---- | -------------------------------- |
| Standard Operating Procedure | SOP  | `Document-Control-SOP.md`        |
| Work Instruction             | WI   | `GitHub-Document-Control.md`     |
| Template / Form              | TPL  | `Design-Review-Form.md`          |
| Record / Evidence            | REC  | `CAPA-Log.md`                    |
| Configuration / Automation   | CFG  | `GH-Issue-Templates.yml`         |
| External Document Metadata   | EXT  | `EXT-ISO-13485-r1.md`            |

---

### **5.2 Embedded QMS Headers**

All QMS-controlled files must include **embedded metadata headers** that identify and control the document.
Headers may be written as YAML front matter, Markdown metadata, or comment blocks depending on file type.

#### **5.2.1 Header Format**

| File Type                         | Header Format                                | Example                                  |
| --------------------------------- | -------------------------------------------- | ---------------------------------------- |
| Markdown (`.md`)                  | YAML front matter block or Markdown metadata | `---\n# FLEY QMS Header\nslug: ...\n---` |
| YAML / JSON                       | YAML keys under a “FLEY QMS Header” comment  | `# FLEY QMS Header\nslug: ...`           |
| HTML / Markdown comment templates | HTML comment block containing header         | `<!-- slug: ..., revision: ... -->`      |

#### **5.2.2 Required Header Fields**

| Field               | Description                                               |
| ------------------- | --------------------------------------------------------- |
| `slug`              | Unique document identifier (e.g., `Document-Control-SOP`) |
| `revision`          | Approved revision identifier (`r#`)                       |
| `type`              | Document type (SOP, WI, TPL, REC, CFG, etc.)              |
| `status`            | One of: `draft`, `approved`                               |
| `effective`         | Effective date (or `null` if pending)                     |
| `controlled_source` | URL of the authoritative repository file                  |
| `related`           | (Optional) Related SOPs, WIs, or documents                |

> Markdown files with legacy headers may retain them until next revision.
> Future updates will standardize on YAML headers.

---

### **5.3 Drafting and Review Workflow**

1. Authors create a feature branch for each new draft or revision:

   ```bash
   git checkout -b update/SOP-Document-Control_r3
   ```
2. Edit the file using the correct header and format.
3. Commit changes with a clear message.
4. Push the branch and open a **Pull Request (PR)** for review.
5. Reviewers comment or approve within the PR.
6. Once all approvals are complete, the PR is merged into `main`.

> The merged commit serves as the official approval record.

---

### **5.4 Tagging Approved Revisions**

After merging, the DCC or Quality Manager creates a tag matching the document slug and revision:

```bash
git tag SOP-Document-Control_r3
git push origin SOP-Document-Control_r3
```

**Rules:**

* Tag names must match slug and revision exactly.
* Tags are immutable and uniquely identify each approved revision.
* Tags represent the effective record of approval.

---

### **5.5 Publication and Controlled Source**

1. The `main` branch (HEAD) represents the **current approved revision** of each document.
2. The repository wiki or equivalent publication surface displays the same content for user access.
3. Users verify document currency by confirming the file matches the `main` branch or latest approved tag.

---

### **5.6 Control of Superseded and Obsolete Documents**

* When a new revision is approved, prior revisions are superseded.
* Superseded revisions remain traceable via **Git tags**.
* Only the latest approved revision exists on the `main` branch.
* Obsolete documents (for discontinued processes) are removed from `main`.
* No “obsolete” status is required in file headers.
* Tags serve as the permanent historical and audit record.
* Users access controlled documents only from the `main` branch or approved publication locations.
* Removal from the controlled source prevents unintended use.

---

### **5.7 Audit Evidence**

* Each file’s QMS header provides identification and revision metadata.
* Git tags, PRs, and commit history provide immutable approval traceability.
* Auditors can confirm compliance by cross-referencing a file’s header, tag, and associated PR.

---

## **6. Records and Retention**

| Record Type                      | Location                   | Retention  |
| -------------------------------- | -------------------------- | ---------- |
| Controlled Markdown Files        | GitHub `main` branch       | Indefinite |
| Tags (approved revisions)        | GitHub repository          | Indefinite |
| Pull Requests (approval records) | GitHub                     | Indefinite |
| Commit history (traceability)    | Git repository             | Indefinite |
| Archived/Obsolete Files          | Git history                | Indefinite |

All GitHub metadata serves as the official QMS record of document control activities.
