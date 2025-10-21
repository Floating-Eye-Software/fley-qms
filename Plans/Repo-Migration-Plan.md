# **PLAN – QMS Repository Architecture and Go-Live Transition**

**Slug:** Repo-Migration-Plan  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Quality-Planning-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan  

---

**Related Documents:**

* WI – GitHub Version Control
* WI – GitHub Change Control
* WI – GitHub QMS Setup
* Plan – Red Witch Pilot SOP Implementation
* Ref – Red Witch QMS Base System Vision

---

## **1. Purpose**

This memo defines the transition plan for restructuring the Red Witch GitHub environment to establish a **dedicated, controlled QMS repository** that supports:

* Branch-based approval workflows (Pull Requests)
* Protected “live” main branch for approved documentation
* Separation between **QMS governance (FLEY QMS)** and **product/web hosting (Red Witch)**

The goal is to move the current QMS working content — which currently lives in the Red Witch **wiki** — into a repository that can be managed and approved using the full GitHub Pull Request process.

---

## **2. Current State (As of Today)**

| Aspect               | Current State                                                                                                        |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Repository:**      | `mlehotay/redwitch`                                                                                                  |
| **Branch:**          | `main` (contains only a basic README)                                                                                |
| **Hosting:**         | GitHub Pages active at **[https://redwitch.ca](https://redwitch.ca)**                                                |
| **Wiki Repository:** | `mlehotay/redwitch.wiki`                                                                                             |
| **Wiki Contents:**   | Complete QMS working content — Quality Manual, SOPs, WIs, Plans, and records — with full commit history.             |
| **Change Control:**  | **Not enforceable** through Pull Requests or branch protection, since wikis cannot use PR-based review or approvals. |

---

## **3. Problem Statement**

The Red Witch wiki has become the working home of the QMS content, but GitHub **wikis are not subject to Pull Requests, branch protections, or review enforcement**.
This means:

* QMS changes cannot follow the formal **Change Request → Branch → Pull Request → Approval → Merge** workflow.
* The wiki’s “live” state updates immediately upon push, without approval gates.
* No branch protection or CODEOWNERS enforcement is possible.

As a result, the QMS cannot yet be brought under proper change control or used as a compliant source of controlled documentation.

---

## **4. Design Decision**

A new dedicated repository, **`fley-qms`**, will be created to serve as the **controlled system of record** for all QMS documentation.

| Repository          | Purpose                                                                        | Change Control Method                                  |
| ------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------ |
| **`fley-qms`**      | Authoritative QMS documents (Quality Manual, SOPs, WIs, Templates, Compliance) | Protected `main` branch, Pull Requests for all changes |
| **`fley-qms.wiki`** | Published read-only view of approved documents                                 | Manual sync from approved `main` branch                |
| **`redwitch`**      | Public web host for redwitch.ca (app, site, landing page)                      | GitHub Pages                                           |
| **`redwitch.wiki`** | Historical QMS content (source of migration)                                   | Will be deprecated after migration                     |

---

## **5. Target Architecture Overview**

```
├── fley-qms/
│   ├── main/ (approved, live QMS)
│   ├── qms-setup/ (imported history from redwitch.wiki)
│   ├── change/* (branches for Change Requests)
│   ├── QMS/
│   ├── SOPs/
│   ├── WIs/
│   ├── Templates/
│   ├── Plans/
│   └── Records/
│
├── fley-qms.wiki/         ← published, read-only view of approved docs
│
├── redwitch/              ← host for redwitch.ca website
│   └── README.md
│
└── redwitch.wiki/         ← current QMS working repo (to be retired)
```

---

## **6. Transition Plan**

### **Phase 1 – Extract and Migrate QMS Source**

1. Clone the current **wiki repo**:

   ```bash
   git clone https://github.com/mlehotay/redwitch.wiki.git
   cd redwitch.wiki
   ```

2. Rename the default branch to `qms-setup`:

   ```bash
   git branch -m master qms-setup
   ```

3. Clean any non-QMS files if necessary.

4. Create a new repository: **`mlehotay/fley-qms`** (empty).

5. Point the local copy to the new repo:

   ```bash
   git remote add fley-qms git@github.com:mlehotay/fley-qms.git
   git push fley-qms qms-setup
   ```

---

### **Phase 2 – Initialize Controlled Baseline**

1. In the `fley-qms` repo, create an **empty `main` branch**:

   ```bash
   git checkout --orphan main
   git rm -rf .
   echo "# FLEY QMS" > README.md
   git add README.md
   git commit -m "Initialize main (empty baseline)"
   git push origin main
   ```

2. **Open a Pull Request**:

   * From: `qms-setup`
   * Into: `main`
   * Title: “Initial QMS Go-Live Baseline”
   * Description: “Migrates QMS documentation from redwitch.wiki to controlled repository.”

3. Review and merge once validated.
   This merge establishes the **official baseline** of the QMS under full Git control.

---

### **Phase 3 – Protect and Configure**

After the PR merges:

* **Protect `main` branch**

  * Require Pull Request review
  * Disallow direct commits and force pushes
  * Enable CODEOWNERS approval

* **Add `CODEOWNERS`**

  ```text
  * @mlehotay
  ```

* **Tag the baseline**

  ```bash
  git tag QMS_Baseline_r1
  git push origin QMS_Baseline_r1
  ```

---

### **Phase 4 – Publish to Wiki**

Once baseline is approved:

1. Clone the `fley-qms.wiki` repository.
2. Copy the Markdown content from `main` into the wiki.
3. Push to publish the **read-only, public view** of the QMS.
4. Link this published wiki in the Red Witch website (`redwitch.ca`) as the official documentation portal.

---

### **Phase 5 – Clean Up Red Witch Wiki**

After the QMS baseline is live:

* Archive `redwitch.wiki` locally (for historical preservation).
* Update `redwitch` README with links:

  * “FLEY QMS Repository: [github.com/mlehotay/fley-qms](https://github.com/mlehotay/fley-qms)”
  * “Published QMS: [github.com/mlehotay/fley-qms/wiki](https://github.com/mlehotay/fley-qms/wiki)”
* Maintain `redwitch` as a lightweight public site host only.

---

## **7. Future Workflow (Post-Migration)**

| Action                | Workflow                                                    |
| --------------------- | ----------------------------------------------------------- |
| **Change Request**    | Create Issue → Branch → Pull Request → Review → Merge → Tag |
| **Controlled Docs**   | Approved version lives in `main` of `fley-qms`              |
| **Publication**       | Manual sync to `fley-qms.wiki` after each approved change   |
| **Backup**            | Export or clone quarterly as QMS record                     |
| **Red Witch Website** | Links to published wiki; no direct QMS content stored       |

---

## **8. Benefits and Rationale**

| Benefit                      | Description                                                                       |
| ---------------------------- | --------------------------------------------------------------------------------- |
| **Preserves Commit History** | All QMS development history from `redwitch.wiki` is retained via migration branch |
| **Proper Change Control**    | PRs, CODEOWNERS, and protected branches enforce formal approval                   |
| **Clean Separation**         | Red Witch web host is now distinct from the controlled QMS repo                   |
| **Stable Publication**       | Wiki serves as static read-only release of approved docs                          |
| **Scalable Structure**       | Supports future automation (auto-publish, version tagging, PDF export)            |

---

## **9. Next Steps**

| Step | Description                                            | Owner |
| ---- | ------------------------------------------------------ | ----- |
| 1    | Clone `redwitch.wiki` and rename branch to `qms-setup` | You   |
| 2    | Create `fley-qms` repo                                 | You   |
| 3    | Push `qms-setup` branch to new repo                    | You   |
| 4    | Create empty `main` branch                             | You   |
| 5    | Submit PR (`qms-setup` → `main`)                       | You   |
| 6    | Protect `main` and configure CODEOWNERS                | You   |
| 7    | Tag baseline (`QMS_Baseline_r1`)                       | You   |
| 8    | Publish approved content to `fley-qms.wiki`            | You   |
| 9    | Update `redwitch` repo and website links               | You   |
