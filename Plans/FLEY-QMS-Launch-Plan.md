MilestonesFLEY-QMS Launch

FLEY-QMS Launch
Closed
No due date
Closed 20 hours ago
100% complete

This is the fley-qms component of the FLEY-QMS Launch milestone.
The redwitch component is here: https://github.com/Floating-Eye-Software/redwitch/milestone/5

### Overview

This milestone represents the formal **go-live** of the Floating Eye Software Quality Management System (FLEY-QMS), completing the migration from the *Red Witch pilot environment* to a fully controlled, organization-managed QMS repository.

The go-live establishes:

* Organizational ownership and team-based access control.
* Enforced branch protection and CODEOWNERS approvals.
* Verified configuration documentation (Repo-Migration-Plan *r2*).
* Effective verification of the migration plan’s results and controls.

### Scope (Issues & Pull Requests)

| ID                                                                          | Title                                             | Type           |
| --------------------------------------------------------------------------- | ------------------------------------------------- | -------------- |
| [redwitch #28](https://github.com/Floating-Eye-Software/redwitch/issues/28) | Create Controlled QMS Repository                  | Change Request |
| [fley-qms #1](https://github.com/Floating-Eye-Software/fley-qms/pull/1)     | FLEY-QMS_r1 – Initial Controlled QMS Baseline     | Pull Request   |
| [fley-qms #2](https://github.com/Floating-Eye-Software/fley-qms/issues/2)   | Create Organization and Update CODEOWNERS         | Change Request |
| [fley-qms #3](https://github.com/Floating-Eye-Software/fley-qms/pull/3)     | Create FLEY Organization and Teams                | Pull Request   |
| [redwitch #7](https://github.com/Floating-Eye-Software/redwitch/issues/7)   | Establish Pull Request Procedure (Change Control) | Procedure / Parent |
| [Repo-Migration-Plan](https://github.com/Floating-Eye-Software/fley-qms/blob/main/Plans/Repo-Migration-Plan.md) | QMS Repository Architecture and Go-Live Transition | Quality Plan |

### Goals

- Transition from the Red Witch pilot environment to the live controlled **FLEY-QMS** repository.
- Create the **FLEY organization**, establish CODEOWNERS, and enforce branch protection rules.
- Execute the **initial controlled QMS baseline** (`FLEY-QMS_r1`) as a formal configuration item.
- Validate that documentation, SOPs, and change control workflows operate under full configuration control.
- Demonstrate audit-ready repository governance aligned with QMS requirements.

#### **Acceptance Criteria**

- Organization and teams configured with correct permissions.
- CODEOWNERS file active and enforcing approval routing.
- Repository protections (branch, review, and tag rules) verified.
- Migration PR #1 merged and tagged *FLEY-QMS_r1*.
- Red Witch #28 closed referencing successful migration.
- Repo-Migration-Plan *r2* updated and verified for effectiveness.
- PR #3 approved and merged using **Merge Commit**.
- Top Management approval documented in PR #3 comment.

### Outcome

Completion of this milestone establishes the **FLEY-QMS** as the authoritative, controlled QMS repository.
It signifies readiness for formal audits and future expansion of SOPs, effectiveness checks, and continuous improvement under the live QMS framework.

**Related Milestone:**
[QMS Foundations (Red Witch)](../../redwitch/milestone/1)
