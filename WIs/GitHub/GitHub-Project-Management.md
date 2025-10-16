# **WI - Project Management Using GitHub**

**Slug:** GitHub-Project-Management  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Project-Management-SOP   
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-Project-Management  

---

### **1. Purpose**

To define the method for planning, executing, monitoring, and closing projects using GitHub tools—specifically **Projects**, **Issues**, **Pull Requests**, **Discussions**, and related repository functions—to ensure projects are effectively controlled and traceable under the Quality Management System (QMS).

---

### **2. Scope**

This WI applies to all projects managed in GitHub under the organization’s QMS, including QMS improvement initiatives, design and development efforts, and process or operational improvement projects.

---

### **3. References**

* QMS-SOP-07 Project Management
* QMS-SOP-06 Planning
* QMS-SOP-05 Leadership
* WI-QMS-09-01 Operating the QMS in GitHub
* ISO 9001:2015, Clauses 4, 5, 6, 8, 9
* GitHub Documentation: [https://docs.github.com](https://docs.github.com)

---

### **4. Responsibilities**

| Role                     | Responsibilities                                                                                |
| ------------------------ | ----------------------------------------------------------------------------------------------- |
| **Project Manager (PM)** | Creates and manages GitHub Projects, defines milestones, assigns Issues, and monitors progress. |
| **Team Members**         | Work on assigned Issues, update task status, and participate in Discussions and Pull Requests.  |
| **Top Management**       | Reviews project status and outcomes via GitHub Projects and Insights dashboards.                |
| **Quality Manager**      | Verifies that project documentation and records demonstrate conformity with QMS requirements.   |

---

### **5. Procedure**

#### **5.1 Overview of GitHub Project Environment**

A typical project workspace on GitHub (example: [https://github.com/mlehotay/redwitch](https://github.com/mlehotay/redwitch)) includes the following tabs and functions:

| GitHub Feature    | Description and QMS Use                                                                                                                                 |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Code**          | Repository for project documentation, deliverables, and controlled files.                                                                               |
| **Issues**        | Used to capture tasks, risks, opportunities, change requests, and nonconformities related to the project. Each Issue represents a unit of planned work. |
| **Pull Requests** | Used for review and approval of document or code changes. Serves as the official change control mechanism.                                              |
| **Discussions**   | Enables threaded dialogue, brainstorming, or project review meetings. May substitute for email chains and serve as communication records.               |
| **Actions**       | Automates workflows such as notifications, document checks, or task updates (optional for automation).                                                  |
| **Projects**      | The Kanban-style project board used to plan and monitor project progress (Backlog → In Progress → Done).                                                |
| **Wiki**          | Used for static documentation—such as the project plan, objectives, or meeting summaries.                                                               |
| **Security**      | Displays repository security settings and dependency alerts (applicable to development projects).                                                       |
| **Insights**      | Provides analytics on activity, progress, and contributor participation. Useful for management reviews.                                                 |
| **Settings**      | Repository administration—used to manage access, branch protection, and integration settings. Controlled by the PM or Admin only.                       |

---

#### **5.2 Project Initiation**

1. **Create a Repository or Project Board**

   * Use the organization’s GitHub account to create a new repository or use an existing one.
   * Enable the *Projects* feature (from the **Projects** tab → *New Project*).
   * Name the project and include a short description and link to the corresponding SOP.

2. **Define Project Objectives and Scope**

   * Record objectives and success criteria in the Project description or Wiki.
   * Create an Issue labeled `Objective` for each measurable project goal.

3. **Identify Stakeholders and Team**

   * Add collaborators under **Settings → Collaborators and Teams**.
   * Assign appropriate permissions (e.g., Read, Write, Admin).

4. **Establish a Risk and Opportunity Register**

   * Create Issues labeled `Risk` or `Opportunity`.
   * Link these Issues to the project board and QMS Risk Register if applicable.

---

#### **5.3 Project Planning**

1. **Create Tasks**

   * Add Issues for each deliverable or activity.
   * Use labels (e.g., `Task`, `Review`, `Blocked`, `Testing`) to categorize.

2. **Configure the Project Board**

   * Add columns such as *Backlog*, *In Progress*, *Review*, and *Done*.
   * Link Issues to the board so that they appear as cards.

3. **Define Milestones**

   * Under the **Issues → Milestones** tab, create key dates or deliverables.
   * Assign Issues to milestones for schedule tracking.

4. **Documentation**

   * Store supporting documentation (e.g., plans, templates, meeting notes) in the **Wiki** or within `/docs` directory in the repository.

---

#### **5.4 Project Execution and Monitoring**

1. **Update Progress**

   * Team members update the status of Issues (move cards across the board or close Issues when completed).
   * The PM monitors board activity and milestone completion.

2. **Hold Periodic Reviews**

   * Use **Discussions** or a designated Wiki page to record meeting summaries and decisions.
   * Record risks mitigated, actions taken, and new opportunities identified.

3. **Change Management**

   * Any scope, schedule, or deliverable change must be implemented via a **Pull Request** following the Change Control WI.
   * Link the PR to the corresponding Issue or milestone.

4. **Automated Tracking (Optional)**

   * Configure **GitHub Actions** for notifications or automatic board updates (e.g., when an Issue closes, move to *Done*).

---

#### **5.5 Project Review and Control**

1. **Performance Reviews**

   * Use **Insights → Pulse** or **Contributors** to review progress metrics.
   * Compare progress against objectives and milestones.

2. **Lessons Learned**

   * Open a **Discussion** labeled `Lessons Learned` to capture feedback.
   * Summarize improvements in the Wiki.

3. **Escalations**

   * Major deviations (delays, failures, scope changes) must be raised as an **Issue** and reviewed by Top Management.

---

#### **5.6 Project Closure**

1. Confirm all deliverables and Issues are complete.
2. Update the Wiki with a final summary (objectives achieved, lessons learned, links to records).
3. Archive or close the GitHub Project Board.
4. Tag the repository (e.g., `ProjectName_Completed_v1.0`) to mark final closure.

---

### **6. Integration with the QMS**

| Related SOP                     | Integration                                            |
| ------------------------------- | ------------------------------------------------------ |
| **QMS-SOP-05 Leadership**       | Management reviews and strategic oversight.            |
| **QMS-SOP-06 Planning**         | Risk and opportunity management, objectives alignment. |
| **QMS-SOP-02 Change Control**   | PR-based control of changes.                           |
| **QMS-SOP-01 Document Control** | Storage and versioning of project records in Git.      |

---

### **7. Records**

| Record Type                  | Location                   | Retention |
| ---------------------------- | -------------------------- | --------- |
| Project board and Issues     | GitHub Projects / Issues   | Permanent |
| Milestones and pull requests | GitHub                     | Permanent |
| Meeting notes and summaries  | Wiki or repository `/docs` | Permanent |
| Lessons learned              | Wiki / Discussion          | Permanent |
| Tag (project closure record) | Repository tags            | Permanent |
