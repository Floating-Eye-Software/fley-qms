# **Work Instruction — Document Control in GitHub**

**WI ID:** WI-GIT-DC-001
**Project:** Red Witch
**Repo(s):**

* `redwitch` → design & development artifacts (code, designs, tests)
* `redwitch.wiki` → QMS process documents (SOPs, WIs, Plans, Records, Compliance pages)

---

## 1. **Purpose**

This Work Instruction defines *how* the Red Witch Project implements **document control** within GitHub repositories and wiki, ensuring compliance with the Document Control SOP (`SOP-QMS-DC-001`) and regulatory requirements (ISO 9001:7.5, ISO 13485:4.2, 21 CFR 820.40).

---

## 2. **Scope**

Applies to all **QMS documents, project documents, and records** created or maintained in the `redwitch` and `redwitch.wiki` GitHub repositories. Includes:

* SOPs, WIs, Plans, Quality Manual, Compliance pages (`redwitch.wiki`)
* Design docs, requirements, code, test artifacts (`redwitch`)
* Records of approvals, reviews, and sign-offs (via GitHub Issues, Pull Requests, and Wiki edits)

---

## 3. **Roles & Responsibilities**

* **Author** → Drafts or updates documents in branches.
* **Reviewer** → Assigned via Pull Request; checks compliance, accuracy, formatting.
* **Approver** → Project Lead or designated Quality Representative; approves PR before merge.
* **Repo Maintainer** → Ensures repository protections are enforced (branch protection, required reviews).

---

## 4. **Process**

### 4.1 Document Creation

1. New documents are created in the appropriate repo:

   * **Process/QMS docs** → `redwitch.wiki`
   * **Design/project artifacts** → `redwitch`
2. Filename convention: `Title-With-Dashes.md` (camel-case words, no spaces).
3. Each document must include:

   * Title
   * Version history
   * References to relevant SOP/standard

---

### 4.2 Version Control

1. All documents are committed via feature branches.
2. Branch naming convention:

   * `doc/<short-title>` for new docs
   * `update/<short-title>` for changes
3. Changes must be submitted as **Pull Requests (PRs)** into `main`.
4. GitHub automatically maintains full version history.

---

### 4.3 Review & Approval

1. At least **one Reviewer** must review each PR.
2. The **Approver** (Project Lead or Quality Rep) must provide explicit approval before merge.
3. Approvals are recorded in the PR history and serve as the **document approval record**.
4. If required, link PR to an **Issue** documenting the change rationale.

---

### 4.4 Publication & Access

1. Once merged, documents in `redwitch.wiki` are considered **controlled and published**.
2. Documents in `redwitch` repo are controlled as design/development artifacts.
3. Both repos are access-controlled via GitHub permissions; only authorized users may commit or approve.

/Compliance/   → external requirements (regs & standards)
/QMS/          → internal top-level definition of the system
/SOPs/         → what must be done
/WIs/          → how it’s done in tools
/Plans/        → project-level tailoring
/Project-Docs/ → project deliverables
/Records/      → audit evidence
/Templates/    → reusable document scaffolding

---

### 4.5 Obsolete Documents

1. Superseded docs must not be deleted.
2. Instead, mark as **Obsolete** at the top of the file.
3. Add a link to the replacement document.
4. GitHub preserves the historical record in the repo.

---

## 5. **Records**

* **Pull Requests** → approval records
* **Issues** → change requests, rationale, CAPA linkage
* **Git commit history** → version history
* **Wiki edit logs** → document change history

---

## 6. **References**

* SOP-QMS-DC-001 — Document Control SOP
* ISO 9001:2015 §7.5
* ISO 13485:2016 §4.2
* 21 CFR 820.40
