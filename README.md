# OpenCart 4.x Storefront – Quality Assurance Project

[![Target System](https://img.shields.io/badge/Target-OpenCart%204.x-blue?style=flat-square)](https://demo.opencart.com)
[![Test Cases](https://img.shields.io/badge/Scripted%20TCs-60%20Executed-success?style=flat-square)](./Test-Cases.md)
[![Pass Rate](https://img.shields.io/badge/Pass%20Rate-91.67%25%20(55%2F60)-brightgreen?style=flat-square)](./Test-Summary-Report.md)
[![Bugs Logged](https://img.shields.io/badge/Bugs%20Logged-8%20(Jira)-critical?style=flat-square)](./Bug-Summary.md)
[![Exploratory](https://img.shields.io/badge/Exploratory-3%20SBTM%20Sessions-informational?style=flat-square)](./Test-Summary-Report.md)

A structured **Manual, Functional, Exploratory, and Regression QA** project validating the **OpenCart 4.x** storefront (`https://demo.opencart.com`), documented with test suites, execution metrics, defect tracking in Jira/Xray, and a prioritized regression checklist.

---

## Project Overview

* **Application Under Test:** OpenCart 4.x E-Commerce Storefront
* **Testing Approach:** Manual Functional, Boundary Value,
  Exploratory, and Regression Test Preparation.
* **Planned Coverage:** 19 functional modules documented
  in the Test Scenarios.
* **Executed Coverage:** 60 scripted test cases across
  9 functional modules, supported by 3 exploratory
  testing sessions.
* **Environment:** Windows PC / Google Chrome.
* **Tools:** Jira, Xray, Microsoft Excel, Git, GitHub.

---

## Key Execution & Defect Metrics

| Metric | Value | Notes |
| :--- | :---: | :--- |
| **Total Scripted Test Cases** | **60** | `TC_001` – `TC_060` across 9 modules |
| **Executed Test Cases** | **60 (100%)** | `OpenCart Execution - Day 1` (30) & `Day 2` (30) |
| **Passed Test Cases** | **55 (91.67%)** | 28 passed on Day 1; 27 passed on Day 2 |
| **Failed Test Cases** | **5 (8.33%)** | 2 failed on Day 1; 3 failed on Day 2 |
| **Not Executed / Blocked** | **0 (0%)** | Full execution coverage achieved |
| **Defects Logged in Jira** | **8** | `PNCRT-90` – `PNCRT-97` (3 Major, 3 Medium, 2 Minor) |

---

## Repository Deliverables & Documentation

| Deliverable | File | Description |
| :--- | :--- | :--- |
| Project Overview | `Project-Overview.md` | Project objectives, scope, and application details. |
| Application Features | `Application-Features.md` | Functional feature breakdown and static testing observations. |
| Test Plan | `Test-Plan.md` | Testing strategy, scope, environment, and criteria. |
| Test Scenarios | `Test-Scenarios.md` | 117 detailed scenarios across 19 functional modules. |
| Test Cases | `Test-Cases.md` | Index of 60 executed scripted test cases. |
| Bug Summary | `Bug-Summary.md` | Summary of 8 reported defects. |
| Test Summary Report | `Test-Summary-Report.md` | Execution results, defect analysis, risks, and final recommendation. |
| Regression Checklist | `regression_checklist.md` | 17 prioritized regression checks prepared for future execution. |

---

## Highlights of Logged Defects (`PNCRT-90` – `PNCRT-97`)

* **Empty Mandatory Option (`PNCRT-92`):** The required `* Select` option dropdown on `Canon EOS 5D` contains no selectable options.
* **Cart Quantity & Totals Anomalies (`PNCRT-95`, `PNCRT-93`):** Updating cart quantity beyond stock (`999999`) triggers a green success banner with unrealistic totals (`PNCRT-95`), while adding a negative quantity (`-2`) to an empty cart displays a misleading success message (`PNCRT-93`).
* **Input Validation & Account/Auth Edge Cases (`PNCRT-90`, `PNCRT-91`, `PNCRT-96`, `PNCRT-94`, `PNCRT-97`):** Password accepts 3 characters below the minimum of 4 (`PNCRT-90`); no warning after >5 failed logins (`PNCRT-91`); case-sensitive email uniqueness check on registration (`PNCRT-96`); silent failure on reviews under 25 characters (`PNCRT-94`); and reusing the exact current password (`PNCRT-97`).

---
## Release Recommendation

**Not Recommended for Production Release**

Although 55 out of 60 scripted test cases passed
(91.67%), 8 unresolved defects were identified and
documented during testing.

Several defects affect important customer journeys,
including product selection, cart quantity validation,
and account registration.

The application should not be considered ready for
production release until the critical functional issues
are addressed and successfully retested.

The prepared regression checklist (17 checks) should
also be executed against the updated build to verify
that existing functionality remains stable.
