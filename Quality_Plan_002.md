Nice — good source SDLC to compare against. I mapped the *Red Witch* Work Instructions + Design Control Plan you gave me to the ISO/IEC/AAMI-style SDLC you supplied, identified where Red Witch already meets the requirement and where there are gaps, and gave concrete, prioritized remediation actions (who should own them and what to deliver). I did this so your team can turn each gap into a next sprint ticket.

# Executive summary

Red Witch already covers many high-level concepts required by the SDLC (DSS phases mapped to Discovery → Alpha → Beta → Live, GitHub-based traceability, CI/CD, accessibility, privacy/security reporting, risk logs, QA/automation).
Major gaps are mostly **operational & evidence** gaps required for medical-device / regulated-software compliance and the AAMI TIR45 application of Agile: clear phase *exit criteria*, formalized **usability engineering & PIAs early**, full **traceability artifacts**, **software safety classification (IEC 62304)**, **change control & release approval process** (particularly emergency changes), **defined RACI for security/privacy/QA**, and explicit **verification/validation (V\&V) plans and records**. These are fixable by adding a small set of templates, checklists, and governance checkpoints.

Below is a mapped gap assessment with prioritized remediation actions.

# Gap assessment (mapped by SDLC phase & topic)

> Legend:
> • **Covered** — Red Witch has the capability described.
> • **Partial** — Red Witch mentions it but lacks detail/artifacts or required controls.
> • **Missing / Weak** — Not present or insufficient for regulated SDLC.

---

## 1) Planning / Project scoping & requirements

SDLC expectations: intended use/users defined, SRS/requirements documented, safety requirements identified, prioritized backlog, development & test standards.

* Status in Red Witch: **Partial**

  * Strengths: Product Manager role, discovery activities, backlog + Kanban, requirements → code traceability called out.
  * Gaps:

    * No formal **Software Requirements Specification (SRS)** template or requirement levels (user requirements, system requirements, safety requirements).
    * No explicit **intended use / indications for use** statement (needed for medical/health context).
    * No documented **software safety classification process** (IEC 62304: class A/B/C determination).
    * No defined **requirement prioritization criteria** that incorporate safety-criticality.
* Priority: **High**
* Recommended remediation:

  1. Create an SRS template (user needs → design inputs → acceptance criteria). Owner: Product Manager + QA Lead.
  2. Add an “Intended Use Statement” artifact in Discovery; require sign-off before Alpha. Owner: Product Manager.
  3. Implement a Software Safety Classification checklist as part of the Planning/Alpha gate (map to IEC 62304). Owner: Quality Lead + Risk Lead.
  4. Update backlog prioritization policy to include safety/severity score. Owner: Product Manager + Risk Lead.
* Deliverables: SRS doc, safety classification record, backlog prioritization rubric.

---

## 2) Risk management (ISO 14971 / IEC 62304)

SDLC expectations: risk management plan, risk log with severity/occurrence/detectability, mitigation verification, traceability to requirements/tests.

* Status in Red Witch: **Partial**

  * Strengths: Risk logs per feature/sprint; references to ISO 14971/IEC 62304.
  * Gaps:

    * No standardized **risk scoring method** documented (severity × occurrence × detectability or equivalent).
    * No formal mapping of **risks → requirements → mitigations → verification tests** (traceability matrix).
    * No explicit requirement that risk mitigations be verified and documented as completed (evidence).
    * No documented timeframe/trigger for risk review escalation (e.g., when to notify regulators/QMS).
* Priority: **High**
* Recommended remediation:

  1. Adopt a standardized risk scoring matrix (document in Risk Management Plan). Owner: Risk Lead / Quality Lead.
  2. Add required fields to the Risk Log: root cause, control, verification evidence, residual risk, risk acceptor. Owner: Risk Lead.
  3. Create automated linking in GitHub (issue → PR → test artifact) so every risk mitigation links to verification. Owner: Devs + DevOps.
  4. Define thresholds for escalation and approval (e.g., residual risk above X requires Quality Lead sign-off). Owner: Quality Lead.
* Deliverables: Risk Management Plan, updated Risk Log template, traceability practice.

---

## 3) Usability engineering (IEC 62366) & privacy (GDPR / PIA / IEC 27701)

SDLC expectations: early and ongoing UE activities, usability engineering file, validation with representative users; PIA/Data protection impact assessment early.

* Status in Red Witch: **Partial → Weak**

  * Strengths: Usability testing, inclusive design cards, privacy/security report in Beta, periodic usability every 3–4 months.
  * Gaps:

    * No **Usability Engineering File** (artifact required by IEC 62366) capturing tasks, hazard-related use errors, mitigations, validation evidence.
    * **PIA / DPIA** not required in Discovery/Alpha (currently privacy reporting starts at Beta).
    * No documented **privacy by design** controls and data flows diagram early.
* Priority: **High**
* Recommended remediation:

  1. Require a Usability Engineering File created in Alpha with hazard analysis and mitigation mapping; validate in Beta. Owner: Usability/UX Lead + Risk Lead.
  2. Conduct DPIA/PIA during Discovery/Alpha and store the PIA record in Wiki. Owner: Privacy Lead (or Security/Privacy Lead).
  3. Add requirement to capture data flow diagrams, data classification, retention, and location in Discovery. Owner: DevOps + Security Lead.
* Deliverables: Usability Engineering File template; PIA template; data flow artefact.

---

## 4) Architecture, design & implementation (IEC 62304 / AAMI TIR45)

SDLC expectations: high-level architecture, interfaces, module decomposition, coding/testing standards, unit/integration/system test artifacts.

* Status in Red Witch: **Partial**

  * Strengths: High-level repository structure, GitFlow, CI/CD, automated testing emphasized.
  * Gaps:

    * No mandatory **architecture/design documentation** template per release (diagrams, interfaces, third-party components).
    * No explicit **software component/module-level requirements and unit verification trace** demanded by IEC 62304.
    * Dependency / 3rd-party BOM and software bill of materials (SBOM) processes are not specified in enough detail (security required).
* Priority: **Medium → High** (higher if regulated device)
* Recommended remediation:

  1. Add required architecture artifact (system context, module decomposition, interfaces) to Alpha deliverables. Owner: Dev Lead + Architect.
  2. Implement SBOM generation and dependency scanning policy (tie to Actions). Owner: Security Lead + DevOps.
  3. Require mapping: module → source files → unit tests → verification results (automated if possible). Owner: QA/Test Lead.
* Deliverables: Architecture doc, SBOM pipeline, module-level V\&V mapping.

---

## 5) Verification & Validation (V\&V) evidence, test coverage (ISO 13485 / IEC 62304)

SDLC expectations: planned tests (unit/integration/system/acceptance), test protocols, pass/fail criteria, test records retained.

* Status in Red Witch: **Partial**

  * Strengths: CI/CD, automated testing, device validation mentioned, PR testing required before merge.
  * Gaps:

    * No **formal V\&V plan or test protocol templates** described; acceptance criteria per requirement not enforced.
    * No guidance for **traceable test evidence** retention and packaging for regulatory submissions (test reports, coverage metrics).
    * No standard for required coverage for safety-critical code or dependency vulnerabilities.
* Priority: **High**
* Recommended remediation:

  1. Produce a V\&V Plan template (maps requirements → test cases → acceptance criteria). Owner: QA Lead.
  2. Enforce PR checklist items that require test evidence links for any requirement touched. Owner: Dev Lead + QA.
  3. Add required test-report artifacts to each release package (unit test summary, integration test report, system test report, UAT report). Owner: QA Lead.
* Deliverables: V\&V Plan, test case templates, CI artifacts retention policy.

---

## 6) Release management & regulatory approvals (Release Phase)

SDLC expectations: release package with documentation, sign-offs, regulatory submission records when applicable, formal release approvals.

* Status in Red Witch: **Partial → Weak**

  * Strengths: GitHub Actions for CI/CD, release tagging, mention of deployment pipelines.
  * Gaps:

    * No **formal Release Approval Board** process or checklist (Product Manager + Quality + Security sign-offs).
    * No clear list of **required contents for a regulated release package** (SRS, risk file, V\&V evidence, Usability File, SBOM, PIA).
    * Regulatory submission workflow and responsibilities (who prepares submission artifacts) are not documented.
* Priority: **High**
* Recommended remediation:

  1. Define a Release Checklist for regulated releases including required sign-offs (Quality Lead, Product Manager, Security/Privacy Lead). Owner: Project Manager + Quality Lead.
  2. Define Release Package contents and add it to GitHub Releases or an audit folder (immutable). Owner: QA Lead.
  3. Document regulatory submission owner and template (for jurisdictions targeted). Owner: Regulatory Lead (or Quality Lead).
* Deliverables: Release Checklist, Release Package template, sign-off workflow.

---

## 7) Change & configuration management (incl. emergency changes)

SDLC expectations: controlled change process, version history, CM records, emergency change path with retrospective controls.

* Status in Red Witch: **Partial**

  * Strengths: GitFlow, tagging releases, branch rules.
  * Gaps:

    * No detailed **change control board (CCB)** process, approval gating for major changes, nor an explicit emergency change process with post-facto documentation.
    * No formal **configuration management records** for builds/artifacts and environment baselines for audit.
* Priority: **High**
* Recommended remediation:

  1. Formalize Change Control Process: change request record, impact analysis, approvals, and traceability. Owner: Project Manager + Quality Lead.
  2. Define Emergency Change Procedure: who approves, what evidence must follow, timeline for retrospective documentation. Owner: Quality Lead.
  3. Retain configuration records (builds, docker images, infrastructure as code versions) in immutable storage. Owner: DevOps.
* Deliverables: Change Control SOP, Emergency Change SOP, CM records policy.

---

## 8) Security, privacy & data governance (IEC 27001 / 27701 / GDPR)

SDLC expectations: threat modeling, dependency scanning, data maps, access controls, logs/audit trails, DPIA, incident response.

* Status in Red Witch: **Partial**

  * Strengths: dependency scanning, vulnerability alerts, privacy & security report per sprint mentioned.
  * Gaps:

    * Threat modeling is not mandated in Discovery/Alpha.
    * PIA is delayed to Beta in your docs — should start earlier.
    * No explicit periodic penetration testing or vulnerability remediation SLA.
    * Access control and audit logging policies are described at a high level but lack procedural detail (who reviews logs, retention).
* Priority: **High**
* Recommended remediation:

  1. Add threat modeling in Discovery or early Alpha (STRIDE or similar). Owner: Security Lead.
  2. Move DPIA/PIA into Discovery/Alpha (privacy by design). Owner: Privacy Lead.
  3. Define vulnerability management SLAs (patching schedule, severity mapping). Owner: Security Lead.
  4. Document access control matrix and audit log retention/review schedule. Owner: Security Lead + DevOps.
* Deliverables: Threat model artefact, DPIA, vulnerability SLA, access control policy.

---

## 9) Documentation & traceability (ISO 13485 / 21 CFR Part 11)

SDLC expectations: complete traceability matrix, electronic records controls, versioning, audit trail, document control.

* Status in Red Witch: **Partial**

  * Strengths: Wiki as central store, emphasis on traceability and versioned history.
  * Gaps:

    * No **explicit traceability matrix template** and enforcement (requirements → risks → design → code → tests → V\&V).
    * No mention of **electronic record integrity controls** (signatures, audit trail retention) for Part 11-like requirements.
    * Document control lifecycle (approval, review frequency, archival) not fully specified.
* Priority: **High**
* Recommended remediation:

  1. Establish a Traceability Matrix template and require it for every regulated feature/release. Owner: QA + Dev Lead.
  2. If Part 11 applies, document audit trail controls and e-signature flows (who can sign, retention). Owner: Quality Lead.
  3. Document Wiki/doc lifecycle: approvals, version retention, archival. Owner: Project Manager.
* Deliverables: Traceability Matrix, Doc Control SOP.

---

## 10) Post-market surveillance & maintenance (Maintenance Phase)

SDLC expectations: monitoring (KPIs, complaints), CAPA, field safety corrective actions, maintenance records.

* Status in Red Witch: **Partial**

  * Strengths: Ongoing usability testing, analytics, maintenance plan, monitoring KPI mention.
  * Gaps:

    * No **formal post-market surveillance (PMS) plan** (complaints intake, trending, CAPA workflow).
    * No formal link from user complaints → risk log → CAPA → verification.
    * No explicit record retention policy for maintenance and incident records.
* Priority: **Medium → High**
* Recommended remediation:

  1. Create a PMS/CAP A SOP: complaint handling, trending analysis, CAPA initiation criteria. Owner: Quality Lead.
  2. Ensure analytics and complaint records feed automatically into the risk/CAPA pipeline. Owner: DevOps + QA.
  3. Define retention period for maintenance logs and incident reports. Owner: Quality Lead.
* Deliverables: PMS plan, CAPA workflow, retention policy.

---

## 11) Training & competence

SDLC expectations: role-specific training, re-training after SOP changes, competency records.

* Status in Red Witch: **Weak**

  * Strengths: Training mentioned; onboarding guides.
  * Gaps:

    * No requirement for **training records tied to SOP updates**, no competency validation (tests/observations).
* Priority: **Medium**
* Recommended remediation:

  1. Add training completion & competency checks for critical roles (QA, Security, Product). Owner: Project Manager + HR/Training.
  2. Link required retraining to SOP changes (e.g., major process update triggers retraining). Owner: Project Manager.
* Deliverables: Training log, short knowledge checks.

---

## 12) Governance & oversight (DSS / regulatory checkpoints)

SDLC expectations: gate reviews, exit criteria, approvals for phase transitions.

* Status in Red Witch: **Partial**

  * Strengths: Governance processes referenced (Digital First Assessments, Architecture Review Board).
  * Gaps:

    * Missing explicit **exit criteria** and approval authority for transitions (e.g., Discovery → Alpha, Alpha → Beta).
    * No documented schedule or responsibility for governance reviews.
* Priority: **High**
* Recommended remediation:

  1. Define exit criteria for each phase (list of artifacts + required sign-offs). Owner: Project Manager + Governance Lead.
  2. Add Governance calendar and gate review owners. Owner: Governance Lead.
* Deliverables: Phase Exit Criteria checklist, Gate Review agenda/template.

---

# Quick prioritized action plan (first 6–8 sprint-sized items)

1. **Create SRS & Requirement templates** (SRS + intended use statement). — Owner: Product Manager. Priority: High.
2. **Define Exit Criteria & Gate Sign-offs** for each DSS phase (Discovery/Alpha/Beta/Live). — Owner: Project Manager. Priority: High.
3. **Formalize Risk Scoring & Traceability** (Risk plan, risk→mitigation→test links). — Owner: Risk Lead. Priority: High.
4. **Implement Usability Engineering File & PIA in Alpha** (templates + mandatory artifacts). — Owner: UX Lead + Privacy Lead. Priority: High.
5. **V\&V Plan & Test Evidence Enforcement** (template + CI links). — Owner: QA Lead. Priority: High.
6. **Release Checklist + Release Package Template** (required documents + sign-offs). — Owner: Quality Lead. Priority: High.
7. **Change Control / Emergency Change SOP** (approval, retrospective evidence). — Owner: Quality Lead + Project Manager. Priority: High.
8. **Threat Modeling & SBOM** (run per major release). — Owner: Security Lead. Priority: High.

(Each item should be made into an Issue in your GitHub project with acceptance criteria and a reviewer from Quality.)

# Suggested templates & artifacts (copy-paste friendly)

* Intended Use Statement template (1–2 lines)
* SRS skeleton: user needs → requirements → acceptance criteria → priority → linked issue ID
* Traceability matrix CSV: requirement\_id, risk\_id, design\_doc\_id, module, PR\_id, test\_case\_id, test\_result\_link
* Risk Log columns: id, description, severity, occurrence, detectability, score, mitigation, owner, verification\_evidence\_link, residual\_risk, acceptor, status
* Usability Engineering File outline: context, user tasks, hazard analysis, mitigations, formative/usability testing sessions, validation summary
* V\&V Plan: mapping, test plans, environment, pass/fail criteria, trace links
* Release Checklist: included docs (SRS, Risk File, Usability File, V\&V reports, SBOM, PIA), sign-offs
* Emergency Change Form: justification, impact, approved\_by, test\_evidence\_post-release

# Who should own what (recommended RACI at high level)

* **Product Manager** — Intended use, SRS sign-off, backlog prioritization.
* **Project Manager** — Phase gating, documentation control, training triggers.
* **Quality Lead** — Risk management plan, V\&V plan, release checklist, CAPA, compliance evidence.
* **Risk Lead** — Risk scoring, residual risk acceptance, risk log maintenance.
* **Usability/UX Lead** — Usability engineering file and testing.
* **Security/Privacy Lead** — Threat models, PIA/DPIA, SBOM, vulnerability SLA.
* **Dev Lead / DevOps** — SBOM pipeline, CI evidence, build immutability, linking artifacts.
* **QA/Test Lead** — Test case creation, automated tests, verification evidence.

# Quick notes about applying AAMI TIR45 (Agile in regulated environment)

Red Witch is already agile and GitHub-centric — that’s positive. To align with TIR45 you must emphasize:

* Continuous planning + incremental delivery (already there) **plus** documented risk-based acceptance for incremental releases.
* Keep the artifacts lightweight but **traceable** and auditable; automated linking in GitHub between issues/PRs/tests will help auditors accept agile artifacts as evidence.

# Minimal “must-fix now” checklist (if you have limited bandwidth)

If you can only do a few things now, do these three immediately (turn them into sprint tickets):

1. **Phase Exit Criteria & Release Checklist** — prevents unsafe releases. (Owner: Project Manager + Quality)
2. **Risk scoring method + Risk→Test traceability** — ensures mitigations are verified. (Owner: Risk Lead)
3. **Usability Engineering File & PIA requirement in Alpha** — addresses early safety/usability and privacy by design. (Owner: UX Lead + Privacy Lead)

# Final thoughts

You’re already far along: your process contains many of the right controls and the GitHub tooling + CI/CD + traceability emphasis are big strengths. The work required is mostly **formalizing artifacts, adding a few governance gates, and enforcing traceability** (i.e., turning informal practice into auditable records). Once you adopt the templates above and create a few required gates (exit criteria, release checklist, emergency change), you’ll be much closer to satisfying ISO 13485 / IEC 62304 / IEC 62366 / ISO 14971 and the privacy/security standards and you’ll be able to present succinct audit packages.

If you want, I can:

* produce the **SRS template**, **traceability matrix**, **Risk Log template**, and **Usability Engineering File** skeleton right now (ready to paste into your Wiki or repo), or
* generate a prioritized GitHub Issue list (30–60 minute sprint plan) you can copy into your project board.

Which of those would you like me to build immediately?
