# OpenCart 4.x Storefront – Quality Assurance Project

[![Target System](https://img.shields.io/badge/Target-OpenCart%204.x-blue?style=flat-square)](https://demo.opencart.com)
[![Test Cases](https://img.shields.io/badge/Scripted%20TCs-60%20Executed-success?style=flat-square)](./Test-Cases.md)
[![Pass Rate](https://img.shields.io/badge/Pass%20Rate-91.67%25%20(55%2F60)-brightgreen?style=flat-square)](./Test-Summary-Report.md)
[![Bugs Logged](https://img.shields.io/badge/Bugs%20Logged-8%20(Jira)-critical?style=flat-square)](./Bug-Summary.md)
[![Exploratory](https://img.shields.io/badge/Exploratory-3%20SBTM%20Sessions-informational?style=flat-square)](./Test-Summary-Report.md)

A structured **Manual, Functional, Exploratory, and Regression QA** project validating the **OpenCart 4.x** storefront (`https://demo.opencart.com`), documented with test suites, execution metrics, defect tracking in Jira/Xray, and a prioritized regression checklist.

---

## Project Overview

* **Application Under Test:** OpenCart 4.x E-Commerce Storefront (`https://demo.opencart.com`)
* **QA Scope:** End-to-end validation across 9 functional areas (`Register_Account`, `Login`, `Logout`, `Forgot_Password`, `Search`, `Product_Display_Page`, `Add_to_Cart`, `Shopping_Cart`, `Checkout`), supported by **3 Session-Based Test Management (SBTM)** exploratory charters and a prioritized **Regression Checklist**.
* **Tools & Stack:** Jira, Xray Test Management, Google Chrome, Markdown Documentation.

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
| **Test Summary Report** | [`Test-Summary-Report.md`](./Test-Summary-Report.md) | Final 7-section QA summary covering scope, execution results, defect analysis, module coverage, risks, and release recommendation. |
| **Test Cases Suite** | [`Test-Cases.md`](./Test-Cases.md) | Complete index of all 60 unique test cases (`TC_001`–`TC_060`) grouped by module with direct Jira issue links. |
| **Bug Summary** | [`Bug-Summary.md`](./Bug-Summary.md) | Master defects log (`PNCRT-90`–`PNCRT-97`) with severity, priority, status, module, and direct Jira links. |
| **Regression Checklist** | [`Regression-Checklist.md`](./Regression-Checklist.md) | 17 prioritized regression checks (`P1` High, `P2` Medium, `P3` Low) for post-fix and build verification. |
| **Raw Exports** | [`Jira.csv`](./Jira.csv), [`Jirabugs.csv`](./Jirabugs.csv), [`execution.csv`](./execution.csv) | Source exports from Jira for full traceability and auditability. |

---

## Highlights of Logged Defects (`PNCRT-90` – `PNCRT-97`)

* **Empty Mandatory Option (`PNCRT-92`):** The required `* Select` option dropdown on `Canon EOS 5D` contains no selectable options.
* **Cart Quantity & Totals Anomalies (`PNCRT-95`, `PNCRT-93`):** Updating cart quantity beyond stock (`999999`) triggers a green success banner with unrealistic totals (`PNCRT-95`), while adding a negative quantity (`-2`) to an empty cart displays a misleading success message (`PNCRT-93`).
* **Input Validation & Account/Auth Edge Cases (`PNCRT-90`, `PNCRT-91`, `PNCRT-96`, `PNCRT-94`, `PNCRT-97`):** Password accepts 3 characters below the minimum of 4 (`PNCRT-90`); no warning after >5 failed logins (`PNCRT-91`); case-sensitive email uniqueness check on registration (`PNCRT-96`); silent failure on reviews under 25 characters (`PNCRT-94`); and reusing the exact current password (`PNCRT-97`).

---

## Release Recommendation

**Conditional Release:** Core storefront flows function reliably (**91.67%** pass rate), but releasing to production should be gated on resolving `Major` defects especially empty mandatory options (`PNCRT-92`), cart quantity/total calculation issues (`PNCRT-95`, `PNCRT-93`), and case-sensitive duplicate account registration (`PNCRT-96`) followed by a run of the [`Regression-Checklist.md`](./Regression-Checklist.md).
