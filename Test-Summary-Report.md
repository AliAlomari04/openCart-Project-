# Test Summary Report – OpenCart 4.x (`demo.opencart.com`)

**Project:** OpenCart 4.x E-Commerce Storefront 
**Target System:** OpenCart 4.x (`https://demo.opencart.com`)  
**Test Management & Execution:** Jira & Xray (`PNCRT` Project)  
**Test Scope:** 60 Scripted Test Cases (`TC_001`–`TC_060`) + 3 Exploratory Testing Sessions (SBTM) + Regression Checklist

---

## 1. Project Overview

This Test Summary Report presents the final quality assurance results for the **OpenCart 4.x** storefront (`https://demo.opencart.com`). The objective of the testing effort was to validate core customer journeys including account registration, authentication, password recovery, product search, product display pages (PDP), cart management, and 6-step checkout as well as boundary conditions, input validations, session security, and responsive UI behavior.

---

## 2. Testing Scope

### In-Scope
* **Scripted Functional & Boundary Test Cases:** 60 test cases (`TC_001`–`TC_060`) executed across two test execution cycles (`OpenCart Execution - Day 1` and `OpenCart Execution - Day 2`) in Xray.
* **Exploratory Testing (SBTM):** 3 time-boxed exploratory charters covering Registration & Account Security, Shopping & Checkout Flows, and Responsive UI / Cross-View Behavior.
* **Regression Test Preparation:** A prioritized regression checklist containing 17 checks (P1–P3) was prepared for future execution after defect fixes. Regression execution was not part of this testing cycle.

### Out-of-Scope / Limitations
* Live payment gateway processing and real financial transactions on the public demo environment.
* Backend admin panel configuration and server-level performance/load testing.
* Public demo environment resets, shared test data states, and third-party edge restrictions (such as anti-bot/Cloudflare challenges on certain automated or repeated requests).

### Execution Limitations

- Cross-browser execution was not included in the
  completed testing cycle.
- Regression testing was not executed during this cycle.
  A prioritized checklist containing 17 regression
  checks was prepared for future execution after fixes.
- The reported results represent the tested public demo
  environment and may be affected by shared test data
  and periodic environment resets.

---

### Responsive UI Testing

Responsive behavior was tested using Google Chrome at
different viewport sizes by manually resizing the viewport
and selecting preset dimensions.

The testing focused on layout consistency, element visibility,
navigation, and usability across different screen sizes.


---


## 3. Test Execution Summary

All **60 scripted test cases** were executed across two execution runs in Xray with **0 test cases left unexecuted**:

| Execution Run | Total Tests | Passed | Failed | Not Executed | Pass Rate |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **OpenCart Execution - Day 1** (`PNCRT-88`) | 30 | 28 | 2 | 0 | 93.33% |
| **OpenCart Execution - Day 2** (`PNCRT-89`) | 30 | 27 | 3 | 0 | 90.00% |
| **Total Execution** | **60** | **55** | **5** | **0** | **91.67%** |

* **Execution Coverage:** 100% (60 / 60 scripted test cases executed).
* **Overall Pass Rate:** 91.67% (55 Passed).
* **Overall Fail Rate:** 8.33% (5 Failed).

---

## 4. Defect Summary

A total of **8 unique defects** (`PNCRT-90` to `PNCRT-97`) were logged in Jira and remain open (`To Do`) on the demo environment:

* **By Jira Priority:** 1 High (`PNCRT-92`), 5 Medium (`PNCRT-90`, `PNCRT-91`, `PNCRT-93`, `PNCRT-95`, `PNCRT-96`), 2 Low (`PNCRT-94`, `PNCRT-97`).
* **By Severity:** 3 Major, 3 Medium, 2 Minor.
* **Notable Findings:**
  * **Empty Mandatory Option (`PNCRT-92`):** The required `* Select` dropdown on `Canon EOS 5D` has no selectable options, blocking valid item selection/cart addition.
  * **Invalid Quantity & Stock Calculation (`PNCRT-95`, `PNCRT-93`):** Updating cart quantity to an extreme value (`999999`) triggers a success banner and unrealistic totals (`PNCRT-95`), while adding a negative quantity (`-2`) to an empty cart displays a misleading success message (`PNCRT-93`).
  * **Validation & Security/Account Edge Cases (`PNCRT-90`, `PNCRT-91`, `PNCRT-96`, `PNCRT-94`, `PNCRT-97`):** Password minimum length allows 3 characters instead of 4 (`PNCRT-90`); no warning is shown after more than 5 failed login attempts (`PNCRT-91`); email uniqueness check is case-sensitive during registration (`PNCRT-96`); submitting a review under 25 characters fails silently (`PNCRT-94`); and changing password to the exact same current password is permitted (`PNCRT-97`).

---

## 5. Module Coverage

The 60 unique test cases (`TC_001`–`TC_060`) are distributed across 9 functional labels/modules as follows (with overall execution totals of **55 Passed** and **5 Failed** verified from Day 1 and Day 2 runs):

| Module / Label | Scripted TCs | Executed | Notes & Related Defects |
| :--- | :---: | :---: | :--- |
| **Register_Account** (`TC_001`–`TC_008`) | 8 | 8 | Password min-length violation (`PNCRT-90`) & case-sensitive email (`PNCRT-96`) |
| **Login** (`TC_009`–`TC_015`) | 7 | 7 | Missing warning after >5 failed attempts (`PNCRT-91`) |
| **Logout** (`TC_016`–`TC_019`) | 4 | 4 | Session termination, UI state & protected page access checks |
| **Forgot_Password** (`TC_020`–`TC_023`) | 4 | 4 | Password reset request, validation & old-password rejection checks |
| **Search** (`TC_024`–`TC_031`) | 8 | 8 | Full/partial search, filters, empty/non-existent queries & compare flow |
| **Product_Display_Page** (`TC_032`–`TC_039`) | 8 | 8 | Empty mandatory option (`PNCRT-92`), negative qty message (`PNCRT-93`), review <25 chars (`PNCRT-94`) |
| **Add_to_Cart** (`TC_040`–`TC_044`) | 5 | 5 | Home, category, compare, wish list & mandatory-option redirect checks |
| **Shopping_Cart** (`TC_045`–`TC_052`) | 8 | 8 | Quantity recalculation, stock limit (`999999`) banner/totals (`PNCRT-95`), remove & checkout navigation |
| **Checkout** (`TC_053`–`TC_060`) | 8 | 8 | 6-step checkout, delivery/billing address, step navigation, validations & out-of-stock block |
| **Total** | **60** | **60** | **55 Passed / 5 Failed (0 Not Executed)**|

---

## 6. Remaining Risks

* **Unresolved Functional & Validation Bugs:** All 8 defects (`PNCRT-90`–`PNCRT-97`) remain open on `demo.opencart.com`, posing risks of incorrect order/cart totals, confusing user feedback, and weak input validation.
* **Account & Authentication Edge Cases:** Case-sensitive duplicate emails (`PNCRT-96`), lack of warning after repeated failed logins (`PNCRT-91`), and allowing identical password reuse (`PNCRT-97`) may cause account confusion or security gaps if left unaddressed in production.
* **Public Demo Environment Volatility:** Shared demo data, periodic resets, and external protections (such as Cloudflare) can affect reproducibility and browser/device testing consistency.

---

## 7. Testing Recommendation

**Recommendation: Not Recommended for Production Release**

The application should not be considered ready for production release until the identified Major defects affecting product selection, cart calculations, and account registration are resolved and successfully retested. The regression checklist should then be executed against the updated build.

While **91.67% (55/60)** of scripted test cases passed and core happy-path flows work, releasing to production with open `Major` issues—specifically empty mandatory product options (`PNCRT-92`), erroneous cart calculations/banners on invalid quantities (`PNCRT-95`, `PNCRT-93`), and case-sensitive email duplication (`PNCRT-96`)—carries unacceptable business and user-experience risk.

Before signing off on a production release:
1. Fix and re-test `PNCRT-92`, `PNCRT-95`, `PNCRT-93`, and `PNCRT-96` (and address remaining validation/security items `PNCRT-90`, `PNCRT-91`, `PNCRT-94`, `PNCRT-97`).
2. Execute the **Regression Checklist** (`REG-01`–`REG-17`) on the updated build to verify no regressions were introduced.
