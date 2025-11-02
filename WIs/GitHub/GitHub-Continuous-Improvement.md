# WI–004: Continuous Improvement & Contribution Work Instruction

**WI ID:** WI–004  
**Revision:** r1  
**Effective Date:** YYYY-MM-DD  
**Owner / Process Responsible:** QMS Lead  
**Approved By:** QMS Manager  
**Controlled Source:** github.com/mlehotay/redwitch.wiki/WIs/WI-004_Continuous-Improvement.md  
**Approved Git Tag:** WI-004_r1

**Related SOP:** SOP–004 Change Control SOP

---

## 1. Purpose

Defines the process for proposing, submitting, reviewing, and approving improvements to QMS artifacts, including GitHub-based documents and templates, ensuring controlled, traceable updates aligned with SOP–004.

---

## 2. Scope

* **Applicability:** Red Witch project GitHub repository and wiki, including all QMS documents, templates, and contributor guidance files.  
* **Exclusions:** CAPA-driven changes (handled separately via CAPA SOP).

---

## 3. Responsibilities

| Role | Responsibilities |
|------|-----------------|
| Contributor | Submit improvement suggestions via GitHub Issue or Discussion; provide rationale and references. |
| QMS Lead / Reviewer | Evaluate, prioritize, and approve improvements; ensure traceability. |
| Approver (per SOP–004) | Authorize formal changes to controlled documents or processes. |

---

## 4. Inputs

| Input | Source | Notes |
|-------|--------|-------|
| Improvement suggestion | GitHub Issue / Discussion | Labeled `improvement`; may reference CI-### in CIP table |
| Related standards / references | SOPs, WIs, Plans, external regulations | Optional, to support evaluation |

---

## 5. Step-by-Step Procedure

### 5.1 Submit an Improvement

1. Open a GitHub **Issue** labeled `improvement`.  
2. Include:
   - Description of the improvement  
   - Rationale / expected impact  
   - References to related SOPs, WIs, or standards  

> Minor suggestions may remain in the Continuous Improvement Plan (CIP) until approved for implementation.

### 5.2 Review & Prioritization

1. QMS Lead evaluates the suggestion:
   - Minor → log in CIP  
   - Controlled change → follow PR process (SOP–004)  
   - CAPA → initiate CAPA SOP  

### 5.3 Implementation via GitHub

1. Create a feature branch for the change:  
   ```bash
   git checkout -b improvement/<short-description>
````

2. Commit changes with meaningful message referencing the Issue and CI ID:

   ```bash
   git commit -m "Fixes #<IssueNumber> – Updated <artifact>"
   ```
3. Submit a Pull Request (PR) per SOP–004. Assign reviewers.

### 5.4 Controlled GitHub Artifacts

All GitHub-based QMS artifacts are treated as controlled documents, including:

| Artifact             | Location                  | Purpose                                                      | Control Method                                            |
| -------------------- | ------------------------- | ------------------------------------------------------------ | --------------------------------------------------------- |
| `CONTRIBUTING.md`    | Root directory `/`        | Work Instruction for contributors on submitting improvements | PR review, Git tag, WI reference                          |
| `README.md`          | Root directory `/`        | High-level overview of project and QMS structure             | PR review, Git tag                                        |
| Issue / PR templates | `.github/ISSUE_TEMPLATE/` | Standardized fields for improvements, CAPAs, or QMS changes  | PR review, WI/SOP reference                               |
| Wiki pages           | `/wiki/`                  | SOPs, WIs, Plans                                             | PR review, WI/SOP reference                               |
| Project Boards       | GitHub Projects           | Evidence of execution and tracking                           | Board configuration documented, linked to issues and SOPs |

**Procedure for Updating Artifacts:**

1. Draft the change in a branch.
2. Reference WI–004 in the PR description.
3. Ensure reviewer(s) confirm alignment with QMS requirements.
4. Merge PR only after approval.
5. Tag commit with WI revision (e.g., `WI-004_r1`).
6. Archive previous version via Git history or release notes.

### 5.5 Verification & Closure

1. Confirm the change meets the intended improvement.
2. Update CIP table (`Continuous-Improvement-Plan.md`) with completion date and reviewer sign-off.
3. Close the GitHub Issue.

---

## 6. Outputs / Results

| Output                       | Destination / Usage            | Notes                      |
| ---------------------------- | ------------------------------ | -------------------------- |
| Approved improvement         | Repository / Wiki              | Traceable via PR and Issue |
| CIP updated                  | Continuous-Improvement-Plan.md | Records completion         |
| Updated controlled artifacts | Root or repository path        | Versioned via Git tag      |

---

## 7. Records / Documentation

* GitHub Issues labeled `improvement`
* Pull Requests implementing improvements
* Approved WI version with Git tag
* Continuous Improvement Plan (wiki)

---

## 8. References

* SOP–004: Change Control SOP
* ISO 9001:2015, Clause 10 – Improvement
* Plan–001: Continuous Improvement Plan

---

## 9. Revision History

| Revision | Date       | Description                                       | Author | Approved By |
| -------- | ---------- | ------------------------------------------------- | ------ | ----------- |
| r1       | YYYY-MM-DD | Initial release including GitHub artifact control | [Name] | [Name]      |
