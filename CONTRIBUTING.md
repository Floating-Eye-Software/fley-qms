# How to Contribute to the Red Witch QMS

Thank you for helping improve our QMS! Follow these steps to submit suggestions or improvements.

---

## 1. Submit an Improvement

1. Open a **GitHub Issue** in this repository.  
2. Use the label: `improvement`.  
3. Include:  
   - What you want to change or improve  
   - Why it matters (rationale)  
   - References (SOP, WI, Plan, or standard if relevant)  

> Minor suggestions may stay in the **Continuous Improvement Plan (CIP)** until implemented.

---

## 2. Review & Approval

* The **QMS Lead** will review your suggestion and decide:  
  - Minor improvement → log in CIP  
  - Controlled change → PR required  
  - Nonconformance → follow CAPA SOP  

---

## 3. Implementing Changes

1. Create a feature branch:  
   ```bash
   git checkout -b improvement/<short-description>
````

2. Commit your changes referencing the issue number:

   ```bash
   git commit -m "Fixes #<IssueNumber> – <Short description>"
   ```
3. Push the branch and open a **Pull Request (PR)**.
4. Assign reviewers; follow the PR process per SOP–004.
5. After approval, merge into `main` and tag if it’s a controlled QMS change.

---

## 4. Tracking & Records

* All approved changes are traceable via GitHub Issues and PRs.
* Continuous Improvement Plan logs suggestions and completions.
* Controlled document updates follow SOP–004.

---

## 5. References

* WI–004: Continuous Improvement & Contribution Work Instruction
* SOP–004: Change Control SOP
* Continuous Improvement Plan
