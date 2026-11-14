# Test Plan — OpenCart (Frontend)

| Document Information | Details |
| :--- | :--- |
| **Project Name** | OpenCart (Frontend) |
| **Document Version** | 1.0 |
| **Prepared By** | Ali Alomari — QA Engineer |
| **Reference Document** | OpenCart Project Functional Requirement Specification (FRS v1.0) |

---

## 1. Introduction
This Test Plan outlines the testing strategy, scope, methodology, environment, criteria, and schedule for testing the **OpenCart Frontend Storefront** (PHP/MySQL/HTML web application). It serves as the governing guideline for validating functional compliance against the FRS document.

---

## 2. Quality & Testing Objectives
* Ensure functional reliability and system assurance across all customer-facing workflows (Registration, Login, Catalog Navigation, Search, Compare, Cart, and Checkout).
* Validate UI alignment, navigation consistency, and usability across supported desktop browsers.
* Identify defects early, document clear reproduction steps with visual evidence, and verify fixes through structured re-testing and regression cycles.

---

## 3. Scope of Testing

### 3.1 In Scope (Functional Modules & Test Levels)
* **Functional Modules:**
  * `Register`, `Login`, `Logout`, and `Forgotten Password`
  * `Home Page` (`Your Store`), `Header`, `Top Menu`, `Slideshow`, `Featured Products`, and `Footer`
  * `Search`, `Category Product Listings`, `Product Compare`, and `Product Detail Page (PDP)`
  * `Add to Cart`, `Wish List`, `Shopping Cart`, and `Currencies`
  * `Checkout` (6-Step Flow), `My Account Page`, `Order History`, `Downloads`, and `Contact Us`
* **Test Levels:**
  * **Smoke / Sanity Testing:** Initial verification of core build stability and readiness.
  * **Functional Testing (Black-Box):** Validating individual requirements using Equivalence Partitioning and Boundary Value Analysis.
  * **Integration Testing:** Verifying combined end-to-end workflows (e.g., Search -> Add to Cart -> Checkout -> Order History).
  * **Cross-Browser Compatibility Testing:** Verifying UI and functional support across Chrome, Edge, and Firefox.
  * **Regression & Re-Testing:** Ensuring defect fixes work as expected and do not break existing functionality (Cart, Checkout Flow).
  * **User Acceptance Testing (UAT):** End-to-end validation from an end-user perspective.

### 3.2 Out of Scope
* **Third-Party Integrations & Payment Gateways:** Security, functional, and transaction processing inside external payment providers (e.g., PayPal, Stripe, Credit Card processors) or external shipping APIs.
* **Backend Admin Dashboard:** Store administration, catalog setup, and CMS settings.
* **Non-Functional & White-Box Testing:** Performance/Load testing, Security penetration testing, Database testing, API testing, and Test Automation.
* **Future Enhancements:** Any feature added outside the baseline FRS v1.0.

---

## 4. Test Strategy & Methodology
This project follows an iterative **Agile methodology** driven by requirement-based testing:
1. **Test Design & Peer Review:** Prepare Test Scenarios, Test Cases, and the **Requirement Traceability Matrix (RTM)** mapped to the FRS. Review coverage and incorporate refinements prior to execution.
2. **Test Execution:** Execute manual test cases against the AUT using predefined test data, comparing `Actual Results` against `Expected Results` to log `Pass`, `Fail`, or `Blocked` statuses.
3. **Defect Logging & Bug Triage:** Log discovered defects in **Jira / Excel** with Severity and Priority ratings, reproduction steps, and screenshots.
4. **Re-Testing & Regression:** Re-test resolved defects on updated builds and execute the Regression Checklist across critical flows (`Cart` & `Checkout`).

---

## 5. Entry, Suspension, and Exit Criteria

### 5.1 Entry Criteria
* FRS document is available, reviewed, and understood by the QA Engineer.
* Test Plan, Test Scenarios, and Test Cases are drafted and reviewed.
* The AUT test environment is deployed, accessible, and passes initial Smoke Testing.
* Required Test Data is prepared.

### 5.2 Suspension & Resumption Criteria
* **Suspension:** Testing will be suspended if a `Blocker` / `Critical` environment failure (e.g., server downtime, database crash, or broken authentication/checkout pipeline) prevents execution of >50% of test cases.
* **Resumption:** Testing resumes once the blocking issue is resolved and the build passes Smoke Verification.

### 5.3 Exit Criteria (Test Completeness)
* 100% of planned manual test cases are executed.
* Requirement Traceability Matrix (RTM) confirms full coverage of in-scope FRS sections.
* All `Critical` / `High` (Severity 1 & 2) defects are documented, resolved, or formally signed off for the next release.
* Test execution evidence, Defect Reports, and the final **Test Summary / Closure Report** are completed.

---

## 6. Test Deliverables

| Phase | Deliverables |
| :--- | :--- |
| **Before Testing** | `Project-Overview.md`, `Application-Features.md`, `Test-Plan.md`, `Test-Scenarios.xlsx`, `Test-Cases.xlsx` |
| **During Testing** | Prepared `Test Data`, `Requirement Traceability Matrix (RTM)`, Execution Logs & Screenshots |
| **After Testing** | Executed `Test-Cases.xlsx` (Pass/Fail), `Bug-Reports.xlsx` / Jira Issues, `Regression-Checklist.md`, `Test-Summary-Report.md` |

---

## 7. Environment & Tools

### 7.1 Testing Tools
* **Test Case Design & Tracking:** Microsoft Excel, Jira & Xray
* **Test Execution:** Manual (Black-Box)
* **Defect Management & Reporting:** Jira, Microsoft Excel, Markdown
* **Configuration Management & Version Control:** Git & GitHub

### 7.2 Hardware & Software Environment
* **Server Stack:** Apache Web Server, PHP 5.4+, MySQL Database
* **Client OS:** Windows 10 / Windows 11 (64-bit)
* **Supported Browsers:** Google Chrome (Latest), Microsoft Edge (Latest), Mozilla Firefox (Latest)

---

## 8. Risks & Assumptions

### Risks
* **Payment & Network Fluctuations:** Payment or checkout steps may fail or time out during network instability.
* **Browser & JavaScript Dependency:** Application UI and dynamic cart dropdowns may fail to load on outdated browsers or when JavaScript is disabled.
* **Demo Environment Constraints:** Public demo servers may reset data periodically or restrict live SMTP email delivery.

### Assumptions
* The test environment remains accessible throughout the scheduled execution window.
* All required testing tools (Jira/Xray, Browsers, Excel) are available and properly configured.

---

## 9. Project Schedule (6-Day Sprint Plan)

| Day | Milestone / Task | Owner | Estimated Effort |
| :--- | :--- | :--- | :--- |
| **Day 25** | Project Understanding, Explore AUT, FRS Review, Overview & Test Plan | Ali Alomari | 1 Day |
| **Day 26** | Requirement Analysis & Writing Positive/Negative Test Scenarios | Ali Alomari | 1 Day |
| **Day 27** | Detailed Test Case Design, Test Data Prep, & RTM Mapping | Ali Alomari | 1 Day |
| **Day 28** | Test Execution (Pass / Fail / Blocked) & Evidence Collection | Ali Alomari | 1 Day |
| **Day 29** | Defect Logging (Bug Reports), Re-Testing, & Regression Testing | Ali Alomari | 1 Day |
| **Day 30** | Final Documentation (`Test-Summary-Report.md`, `Regression-Checklist.md`) & GitHub/Jira Publish | Ali Alomari | 1 Day |

---

## 10. Terms & Acronyms

| Acronym | Definition |
| :--- | :--- |
| **AUT** | Application Under Test |
| **FRS** | Functional Requirement Specification |
| **PDP** | Product Detail Page |
| **QA** | Quality Assurance |
| **RTM** | Requirement Traceability Matrix |
| **UAT** | User Acceptance Testing |