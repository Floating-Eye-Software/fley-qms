# Red Witch Project Management

## Introduction

Red Witch utilizes GitHub's suite of project management tools to streamline collaboration, version control, documentation, and automation. This procedure outlines best practices for leveraging various GitHub components to effectively manage the Red Witch project.

## Code

### GitHub Repository

- All project source code, documentation, and assets are stored in GitHub repositories.
- Each major component of the project has its own repository to facilitate organization and modularity.

#### Key Practices
- **Repository Structure**: Maintain a clear and consistent structure within repositories for easy navigation and access to project assets.
- **Branching Strategy**: Utilize a branching strategy such as GitFlow to manage development and release cycles efficiently.
- **Commit Messages**: Enforce clear and descriptive commit messages to document changes effectively and ensure traceability.

## Issues

### GitHub Issues

- GitHub Issues are used for tracking tasks, bugs, and feature requests, ensuring transparency and accountability.

#### Key Practices
- **Detailed Descriptions**: Provide detailed descriptions for each issue, including steps to reproduce and expected behavior.
- **Assignment and Labels**: Assign issues to team members and categorize them using appropriate labels.
- **Linking**: Link issues to related pull requests, project boards, and milestones for traceability.

## Pull Requests

### Pull Requests (PRs)

- Pull Requests facilitate code review and quality control, allowing for proposed changes to be discussed before merging into the main branch.

#### Key Practices
- **Code Reviews**: Conduct thorough code reviews to ensure code quality and adherence to coding standards.
- **Continuous Integration**: Integrate CI tools like GitHub Actions to automate testing and checks on each PR.
- **Merge Policies**: Define merge policies, requiring a successful build and passing tests before merging code changes.

## Discussions

### GitHub Discussions

- GitHub Discussions foster open-ended conversations and community engagement, facilitating collaboration and idea exchange.

#### Key Practices
- **Community Engagement**: Encourage stakeholders and contributors to participate in discussions, sharing insights and feedback.
- **Idea Generation**: Use discussions to generate new ideas, gather feedback, and make decisions collaboratively.

## Actions

### GitHub Actions

- GitHub Actions automate workflows, such as testing and deployment, improving efficiency and consistency.

#### Key Practices
- **Automated Testing**: Set up automated testing to run on each commit and PR, detecting issues early in the development cycle.
- **Deployment Pipelines**: Configure deployment pipelines to automate the deployment process to various environments (e.g., staging, production).
- **Monitoring and Alerts**: Implement monitoring and alerting within workflows to quickly identify and address issues in production.

## Projects

### GitHub Projects

- GitHub Projects provide Kanban-style boards for managing tasks and workflow, enabling efficient project tracking and progress visualization.

#### Key Practices
- **Kanban Boards**: Utilize Kanban boards within GitHub Projects to visualize tasks and their progress through different stages.
- **Milestones**: Define milestones for major deliverables, tracking progress towards key project goals.
- **Labels**: Categorize tasks using labels (e.g., bug, enhancement, high priority) to facilitate organization and prioritization.

## Wiki

### GitHub Wiki

- GitHub Wikis serve as a central repository for project documentation, including design documents, user guides, and FAQs.

#### Key Practices
- **Structured Documentation**: Organize the Wiki with clear sections, ensuring easy navigation and access to relevant information.
- **Versioning**: Maintain version control for documentation, updating it regularly to reflect project developments.

## Security

### GitHub's Security Features

- Utilize GitHub's security features, such as vulnerability scanning and dependency analysis, to protect the project and ensure compliance with relevant standards.

#### Key Practices
- **Dependency Management**: Regularly update dependencies and address security vulnerabilities to mitigate potential risks.
- **Security Scanning**: Enable security scanning tools to identify and address potential vulnerabilities in the codebase proactively.

## Insights

### GitHub Insights

- GitHub Insights provide analytics and metrics, such as repository traffic and contributor activity, to gain valuable insights into project performance.

#### Key Practices
- **Performance Metrics**: Define and monitor performance metrics to track project progress and identify areas for improvement.

## Settings

### GitHub Repository Settings

- Access repository settings to manage permissions, integrations, and other configuration options for effective project management.

#### Key Practices
- **Access Control**: Define access levels for repositories based on sensitivity and project requirements, ensuring appropriate access control.
- **Integration Management**: Manage integrations and configurations to streamline project workflows and enhance collaboration.

By following these practices and utilizing GitHub's comprehensive set of tools, Red Witch ensures a streamlined and efficient project management process, fostering collaboration, transparency, and innovation.


------


3. Where Project Management Comes In

Now, you asked: “Am I talking about a project management SOP?”

Project Management SOP (if you had one) would define how the project itself is planned, executed, monitored, and reported, including things like:

How backlog items are created from requirements

How sprint planning is done

How issues are tracked on GitHub

How progress is reported to stakeholders

Your situation: The “work” (implementing requirements) is performed via the Design Control SOP. The management of that work (tracking it as issues, planning sprints, moving through Kanban columns) would be covered by a project management SOP or work instruction, if your organization required one.

So:

Design Control SOP → governs how to perform design changes (the actual work).

Project Management SOP / WI → governs how to plan, track, and report that work (workflow management, sprint planning, GitHub issue procedures).



2. Project Management SOP / Work Instructions (WKI)

This is where the planning and execution of the project itself is governed.

Project Management SOP:

High-level rules for managing projects.

May state: “Projects should be managed using GitHub Projects, issues, and sprints.”

Defines responsibilities, reporting cadence, and artifacts (project wiki, boards).

Project Management WKI (Work Instruction):

Step-by-step how-to for this particular project (Red Witch).

Examples of instructions it could contain:

Create the Red Witch repository and project board on GitHub.

Create the Red Witch wiki and add project documentation.

Break requirements into issues on the project board.

Organize issues into sprints or Kanban columns.

Track progress according to the sprint plan and update the wiki.





Exactly — now you’ve landed on the **right concept**. Let’s clarify and tie all the pieces together.

---

### 1. **Project Initiation Document / Project Charter**

* **Purpose:** Formally authorizes the project and defines **what the project is, why it exists, and its high-level objectives**.
* **Key Elements:**

  * Project objectives and scope
  * High-level requirements (sometimes called **design inputs**)
  * Stakeholders and roles
  * High-level schedule, milestones, and resources
  * Authorization to proceed

In your workflow:

* **Design inputs (requirements)** are captured **as part of the charter or initiation record**.
* The charter is essentially **the official “green light”** to start creating work items, sprints, and project-specific artifacts.

---

### 2. **Where the SOPs and Project Docs Fit**

| Concept                            | Where it Lives                                | Purpose                                                      |
| ---------------------------------- | --------------------------------------------- | ------------------------------------------------------------ |
| Design inputs / requirements       | Project Charter / Project Initiation Document | High-level requirements that kick off the project            |
| How design changes are implemented | Design Control SOP                            | Governs the controlled steps to implement changes            |
| How work is tracked / managed      | Project Management SOP / WKI                  | Step-by-step workflow: GitHub setup, issues, sprints, boards |
| Project-specific documentation     | Project Wiki (Red Witch)                      | Detailed architecture, backlog, workflow instructions        |

---

### 3. **Flow of Work**

1. **Project Charter / Initiation Document:** Defines the project, design inputs, and authorizes work.
2. **Design Control SOP:** Any design changes or work derived from those inputs must follow the controlled process.
3. **Project Management SOP/WKI:** Specifies how to organize, plan, and track that work (GitHub issues, sprints, wiki).
4. **Red Witch Wiki:** Contains project-specific implementation details, documentation, and backlog.

---

✅ **Key Insight:**

The **charter is the starting point** — it authorizes the project, defines the initial requirements, and triggers all downstream processes: design control, project management workflow, and sprint planning.

---

If you want, I can make a **single visual diagram** showing **charter → design inputs → design control → project management → GitHub wiki/backlog/sprints**. It usually makes these relationships instantly clear.

Do you want me to do that?
