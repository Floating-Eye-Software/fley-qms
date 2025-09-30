# 🛠 Work Instructions – Project & Quality Planning

These Work Instructions (WIs) define how to implement the **Project & Quality Planning SOP** using GitHub tools.  
If tools change in the future, equivalent workflows must be created to satisfy the SOP requirements.

---

## **1. Project Plans**

### 1.1 Creating a Project Plan
1. Create a new wiki page under `/Project-Docs/` using the naming convention:  
   `Project-Name-Quality-Plan.md`  
2. Include required elements:  
   - Scope and deliverables  
   - Resources and responsibilities  
   - Schedule, phases, and milestones  
   - Risk management approach  
   - Links to quality objectives and compliance requirements  
3. Link the wiki page in the **project’s README** or summary page.  

---

## **2. Quality Plans**

### 2.1 Org-Level Quality Plan
1. Store org-level plans in `/Plans/` (e.g., `Continuous-Improvement-Plan.md`).  
2. Ensure the plan links to:  
   - Applicable standards and regulations  
   - Quality objectives  
   - Metrics and assurance activities  
   - Relevant milestones  

### 2.2 Project-Level Quality Plan
1. Store in `/Project-Docs/`.  
2. Include design and development planning sections.  
3. Link to:  
   - Project milestones  
   - Issues for deliverables  
   - Evidence locations (wiki, PRs, CI/CD logs).  

---

## **3. Issues**

### 3.1 Creating Issues
1. For each deliverable, create an **Issue** in GitHub.  
2. Use the following template fields:  
   - **Title**: Clear deliverable name (e.g., *“Draft Design Control SOP”*).  
   - **Description**: Summary of work, objectives, and acceptance criteria.  
   - **Checklist**: Break into tasks or sub-deliverables.  
   - **Labels**: Use QMS-related labels (`SOP`, `WI`, `CAPA`, etc.).  
   - **Assignees**: Owner responsible for completion.  

### 3.2 Linking Issues
- Link Issues to Milestones (see section 4).  
- Reference Issues from relevant wiki pages using absolute links:  
  `[Draft Design Control SOP](https://github.com/<org>/<repo>/issues/42)`  

---

## **4. Milestones**

### 4.1 Creating a Milestone
1. Navigate to **Issues → Milestones → New Milestone**.  
2. Title: Clear, descriptive (e.g., *“QMS Foundations”*).  
3. Description must include:  
   - **Purpose**  
   - **Scope** (list issues or deliverables)  
   - **Goals**  
   - **Acceptance Criteria**  
   - **Links to Quality Plans or SOPs**  
4. Assign a due date (or “no date” if ongoing).  
5. Save milestone.  

### 4.2 Linking Milestones
- Link milestone pages in Quality Plans, e.g.:  
  `[QMS Foundations](https://github.com/<org>/<repo>/milestone/1)`  

### 4.3 Closing Milestones
1. Verify all associated issues are closed.  
2. Confirm acceptance criteria are met (per Quality Manager).  
3. Close milestone and note closure in the relevant Quality Plan.  

---

## **5. Project Boards**

### 5.1 Creating a Project Board
1. Navigate to **Projects → New Project**.  
2. Select *Kanban* template.  
3. Name: e.g., *“Red Witch QMS Board”*.  
4. Add columns: *Backlog, In Progress, Review, Done*.  

### 5.2 Adding Issues to Board
1. From the Issue, select **Projects → Add to Project**.  
2. Assign to the relevant column.  

### 5.3 Tracking Progress
- Use board views to monitor QMS documentation progress.  
- Reference board in Quality Plans:  
  `[Red Witch Kanban](https://github.com/users/<org>/projects/3)`  

---

## **6. Documentation & Records**

### 6.1 Wiki Structure
- `/Plans/` → Org-level Quality Plans (e.g., Continuous Improvement Plan).  
- `/Project-Docs/` → Project-specific Quality Plans.  
- `/Compliance/` → Regulatory mapping documents.  
- `/SOPs/` → Standard Operating Procedures (tool-agnostic).  
- `/WIs/` → Tool-specific Work Instructions.  

### 6.2 Storing Evidence
- Issues = task records and CAPA evidence.  
- Pull Requests = design review and change control evidence.  
- Wiki pages = formal SOPs, WIs, Plans, and Reports.  
- CI/CD logs = testing, verification, and build evidence.  

---

## **7. Approval & Review**

1. Project Plans and Quality Plans must be approved via Pull Request to the wiki.  
2. Use at least one reviewer from the Quality Manager or designated compliance owner.  
3. Record approvals in the Pull Request history.  
4. Closed milestones must be reviewed for completeness during management reviews.  
