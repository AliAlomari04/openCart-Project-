# Test Cases Suite – OpenCart 4.x (`demo.opencart.com`)

**Project:** OpenCart 4.x E-Commerce Storefront  
**Target System:** OpenCart 4.x (`https://demo.opencart.com`)  
**Issue Tracker:** Jira (`PNCRT` Project)  
**Total Unique Test Cases:** 60 (`TC_001` – `TC_060`) across 9 Modules

---

## Suite Overview by Module

| Module / Label | Test Case Range | Count |
| :--- | :---: | :---: |
| **Register_Account** | `TC_001` – `TC_008` | 8 |
| **Login** | `TC_009` – `TC_015` | 7 |
| **Logout** | `TC_016` – `TC_019` | 4 |
| **Forgot_Password** | `TC_020` – `TC_023` | 4 |
| **Search** | `TC_024` – `TC_031` | 8 |
| **Product_Display_Page** | `TC_032` – `TC_039` | 8 |
| **Add_to_Cart** | `TC_040` – `TC_044` | 5 |
| **Shopping_Cart** | `TC_045` – `TC_052` | 8 |
| **Checkout** | `TC_053` – `TC_060` | 8 |
| **Total** | **`TC_001` – `TC_060`** | **60** |

---

## 1. Register_Account (`TC_001` – `TC_008`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_001** | `PNCRT-28` | Verify registering a new account with valid mandatory fields only | [PNCRT-28](https://iam0engr4ali.atlassian.net/browse/PNCRT-28) |
| **TC_002** | `PNCRT-29` | Verify registration fails when using an already registered E-Mail address | [PNCRT-29](https://iam0engr4ali.atlassian.net/browse/PNCRT-29) |
| **TC_003** | `PNCRT-30` | Verify registration is blocked when all mandatory fields are valid but Privacy Policy is unchecked | [PNCRT-30](https://iam0engr4ali.atlassian.net/browse/PNCRT-30) |
| **TC_004** | `PNCRT-31` | Verify lower boundary validation on Password field (3 characters - below min limit of 4) | [PNCRT-31](https://iam0engr4ali.atlassian.net/browse/PNCRT-31) |
| **TC_005** | `PNCRT-32` | Verify validation error messages when submitting the Register form with all mandatory fields empty | [PNCRT-32](https://iam0engr4ali.atlassian.net/browse/PNCRT-32) |
| **TC_006** | `PNCRT-33` | Verify registering a new account with valid mandatory fields and optional Newsletter subscription checked | [PNCRT-33](https://iam0engr4ali.atlassian.net/browse/PNCRT-33) |
| **TC_007** | `PNCRT-34` | Verify upper boundary validation on First Name field (33 characters - exceeding max limit of 32) | [PNCRT-34](https://iam0engr4ali.atlassian.net/browse/PNCRT-34) |
| **TC_008** | `PNCRT-35` | Verify validation error when entering an invalid E-Mail address format | [PNCRT-35](https://iam0engr4ali.atlassian.net/browse/PNCRT-35) |

---

## 2. Login (`TC_009` – `TC_015`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_009** | `PNCRT-1` | Verify logging in with valid registered E-Mail Address and valid Password | [PNCRT-1](https://iam0engr4ali.atlassian.net/browse/PNCRT-1) |
| **TC_010** | `PNCRT-2` | Verify login failure when using an unregistered E-Mail Address | [PNCRT-2](https://iam0engr4ali.atlassian.net/browse/PNCRT-2) |
| **TC_011** | `PNCRT-3` | Verify login failure when using valid E-Mail with invalid Password, or both invalid | [PNCRT-3](https://iam0engr4ali.atlassian.net/browse/PNCRT-3) |
| **TC_012** | `PNCRT-4` | Verify login failure when submitting the Login form with empty E-Mail and Password fields | [PNCRT-4](https://iam0engr4ali.atlassian.net/browse/PNCRT-4) |
| **TC_013** | `PNCRT-5` | Verify password case-sensitivity by attempting to log in with inverted character casing | [PNCRT-5](https://iam0engr4ali.atlassian.net/browse/PNCRT-5) |
| **TC_014** | `PNCRT-6` | Verify account lockout state transition after exceeding maximum failed login attempts (5 attempts) | [PNCRT-6](https://iam0engr4ali.atlassian.net/browse/PNCRT-6) |
| **TC_015** | `PNCRT-7` | Verify clicking 'Forgotten Password' link redirects to 'Forgot Your Password?' page | [PNCRT-7](https://iam0engr4ali.atlassian.net/browse/PNCRT-7) |

---

## 3. Logout (`TC_016` – `TC_019`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_016** | `PNCRT-8` | Verify logging out via Header 'My Account' dropdown and redirecting to Home Page via 'Continue' | [PNCRT-8](https://iam0engr4ali.atlassian.net/browse/PNCRT-8) |
| **TC_017** | `PNCRT-9` | Verify 'Logout' option is hidden and 'Register'/'Login' options reappear after logging out | [PNCRT-9](https://iam0engr4ali.atlassian.net/browse/PNCRT-9) |
| **TC_018** | `PNCRT-10` | Verify logged-out user cannot access protected 'My Account' pages via browser Back button or direct URL | [PNCRT-10](https://iam0engr4ali.atlassian.net/browse/PNCRT-10) |
| **TC_019** | `PNCRT-11` | Verify logging out in one browser tab invalidates the active session in another open tab | [PNCRT-11](https://iam0engr4ali.atlassian.net/browse/PNCRT-11) |

---

## 4. Forgot_Password (`TC_020` – `TC_023`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_020** | `PNCRT-47` | Verify requesting a password reset using a valid registered E-Mail Address | [PNCRT-47](https://iam0engr4ali.atlassian.net/browse/PNCRT-47) |
| **TC_021** | `PNCRT-48` | Verify completing the password reset flow via confirmation link and logging in with new password | [PNCRT-48](https://iam0engr4ali.atlassian.net/browse/PNCRT-48) |
| **TC_022** | `PNCRT-49` | Verify error message when submitting a non-registered E-Mail Address on Forgot Password page | [PNCRT-49](https://iam0engr4ali.atlassian.net/browse/PNCRT-49) |
| **TC_023** | `PNCRT-50` | Verify user cannot log in using the old password after successfully resetting the password | [PNCRT-50](https://iam0engr4ali.atlassian.net/browse/PNCRT-50) |

---

## 5. Search (`TC_024` – `TC_031`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_024** | `PNCRT-12` | Verify searching for an existing product using its full exact product name | [PNCRT-12](https://iam0engr4ali.atlassian.net/browse/PNCRT-12) |
| **TC_025** | `PNCRT-13` | Verify searching for existing products using partial keywords | [PNCRT-13](https://iam0engr4ali.atlassian.net/browse/PNCRT-13) |
| **TC_026** | `PNCRT-14` | Verify triggering product search using both the Search icon button and keyboard 'Enter' key | [PNCRT-14](https://iam0engr4ali.atlassian.net/browse/PNCRT-14) |
| **TC_027** | `PNCRT-15` | Verify search functionality returns consistent results for both Guest and Logged-in users | [PNCRT-15](https://iam0engr4ali.atlassian.net/browse/PNCRT-15) |
| **TC_028** | `PNCRT-16` | Verify advanced search filtering by Category, 'Search in subcategories', and 'Search in product descriptions' | [PNCRT-16](https://iam0engr4ali.atlassian.net/browse/PNCRT-16) |
| **TC_029** | `PNCRT-17` | Verify message displayed when searching for a non-existing or misspelled product name | [PNCRT-17](https://iam0engr4ali.atlassian.net/browse/PNCRT-17) |
| **TC_030** | `PNCRT-18` | Verify search behavior when submitting an empty Search box | [PNCRT-18](https://iam0engr4ali.atlassian.net/browse/PNCRT-18) |
| **TC_031** | `PNCRT-19` | Verify end-to-end navigation from Search Results to Product Compare and adding item directly to Cart | [PNCRT-19](https://iam0engr4ali.atlassian.net/browse/PNCRT-19) |

---

## 6. Product_Display_Page (`TC_032` – `TC_039`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_032** | `PNCRT-59` | Verify navigating to PDP and displaying accurate product details (Title, Brand, Code, Availability, Price) | [PNCRT-59](https://iam0engr4ali.atlassian.net/browse/PNCRT-59) |
| **TC_033** | `PNCRT-60` | Verify adding a product to the Shopping Cart from PDP with default quantity ('1') | [PNCRT-60](https://iam0engr4ali.atlassian.net/browse/PNCRT-60) |
| **TC_034** | `PNCRT-61` | Verify adding a product to the Shopping Cart from PDP with custom quantity greater than 1 | [PNCRT-61](https://iam0engr4ali.atlassian.net/browse/PNCRT-61) |
| **TC_035** | `PNCRT-62` | Verify adding a product with mandatory 'Available Options' selected (e.g., Color dropdown) | [PNCRT-62](https://iam0engr4ali.atlassian.net/browse/PNCRT-62) |
| **TC_036** | `PNCRT-63` | Verify validation error when clicking 'Add to Cart' without selecting mandatory 'Available Options' | [PNCRT-63](https://iam0engr4ali.atlassian.net/browse/PNCRT-63) |
| **TC_037** | `PNCRT-64` | Verify lower boundary validation on PDP Quantity field when entering '0' (Min - 1) | [PNCRT-64](https://iam0engr4ali.atlassian.net/browse/PNCRT-64) |
| **TC_038** | `PNCRT-65` | Verify validation behavior on PDP Quantity field when entering negative numbers, blank, or non-numeric text | [PNCRT-65](https://iam0engr4ali.atlassian.net/browse/PNCRT-65) |
| **TC_039** | `PNCRT-66` | Verify lower boundary validation on Product Review text (< 25 characters) | [PNCRT-66](https://iam0engr4ali.atlassian.net/browse/PNCRT-66) |

---

## 7. Add_to_Cart (`TC_040` – `TC_044`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_040** | `PNCRT-67` | Verify adding product from Home Featured section displays green banner and updates Header Cart counter | [PNCRT-67](https://iam0engr4ali.atlassian.net/browse/PNCRT-67) |
| **TC_041** | `PNCRT-68` | Verify adding a product to the Shopping Cart from Category Listing page (Grid & List views) | [PNCRT-68](https://iam0engr4ali.atlassian.net/browse/PNCRT-68) |
| **TC_042** | `PNCRT-69` | Verify adding a product to the Shopping Cart directly from the Product Comparison page | [PNCRT-69](https://iam0engr4ali.atlassian.net/browse/PNCRT-69) |
| **TC_043** | `PNCRT-70` | Verify adding a product to the Shopping Cart directly from 'My Wish List' page | [PNCRT-70](https://iam0engr4ali.atlassian.net/browse/PNCRT-70) |
| **TC_044** | `PNCRT-71` | Verify clicking 'Add to Cart' on a product with mandatory options from Featured redirects to PDP | [PNCRT-71](https://iam0engr4ali.atlassian.net/browse/PNCRT-71) |

---

## 8. Shopping_Cart (`TC_045` – `TC_052`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_045** | `PNCRT-72` | Verify navigating to Shopping Cart via Header/Dropdown/Banner links and verifying table columns & weight | [PNCRT-72](https://iam0engr4ali.atlassian.net/browse/PNCRT-72) |
| **TC_046** | `PNCRT-73` | Verify updating product quantity in Shopping Cart recalculates Line Total, Sub-Total, VAT, and Grand Total | [PNCRT-73](https://iam0engr4ali.atlassian.net/browse/PNCRT-73) |
| **TC_047** | `PNCRT-74` | Verify removing a product from Shopping Cart using the red 'Remove' button | [PNCRT-74](https://iam0engr4ali.atlassian.net/browse/PNCRT-74) |
| **TC_048** | `PNCRT-75` | Verify updating quantity to '0' or negative value in Shopping Cart removes the item | [PNCRT-75](https://iam0engr4ali.atlassian.net/browse/PNCRT-75) |
| **TC_049** | `PNCRT-76` | Verify warning banner and '***' indicator when cart quantity exceeds available stock | [PNCRT-76](https://iam0engr4ali.atlassian.net/browse/PNCRT-76) |
| **TC_050** | `PNCRT-77` | Verify error message when applying an invalid or empty Coupon Code in Shopping Cart | [PNCRT-77](https://iam0engr4ali.atlassian.net/browse/PNCRT-77) |
| **TC_051** | `PNCRT-78` | Verify 'Continue Shopping' button on Shopping Cart redirects back to the Home Page | [PNCRT-78](https://iam0engr4ali.atlassian.net/browse/PNCRT-78) |
| **TC_052** | `PNCRT-79` | Verify 'Checkout' button on Shopping Cart redirects to the 6-Step Checkout page | [PNCRT-79](https://iam0engr4ali.atlassian.net/browse/PNCRT-79) |

---

## 9. Checkout (`TC_053` – `TC_060`)

| TC ID | Jira Key | Test Scenario / Objective | Jira Link |
| :--- | :---: | :--- | :--- |
| **TC_053** | `PNCRT-20` | Verify end-to-end 6-Step Checkout as a Logged-in customer until Order Confirmation | [PNCRT-20](https://iam0engr4ali.atlassian.net/browse/PNCRT-20) |
| **TC_054** | `PNCRT-21` | Verify Checkout with separate Delivery Address when 'My delivery and billing addresses are the same' is unchecked | [PNCRT-21](https://iam0engr4ali.atlassian.net/browse/PNCRT-21) |
| **TC_055** | `PNCRT-22` | Verify accordion allows revisiting and editing a previous Checkout step before Confirm Order | [PNCRT-22](https://iam0engr4ali.atlassian.net/browse/PNCRT-22) |
| **TC_056** | `PNCRT-23` | Verify validation error messages when mandatory fields in Billing/Delivery Details are left blank | [PNCRT-23](https://iam0engr4ali.atlassian.net/browse/PNCRT-23) |
| **TC_057** | `PNCRT-24` | Verify validation error when entering invalid format/length in Checkout Post Code or Address fields | [PNCRT-24](https://iam0engr4ali.atlassian.net/browse/PNCRT-24) |
| **TC_058** | `PNCRT-25` | Verify Checkout Step 5 blocks progression with warning banner when 'Terms & Conditions' is unchecked | [PNCRT-25](https://iam0engr4ali.atlassian.net/browse/PNCRT-25) |
| **TC_059** | `PNCRT-26` | Verify Checkout is blocked when Shopping Cart contains an out-of-stock ('***') product | [PNCRT-26](https://iam0engr4ali.atlassian.net/browse/PNCRT-26) |
| **TC_060** | `PNCRT-27` | Verify attempting to navigate to Checkout with an empty Shopping Cart redirects to empty cart view | [PNCRT-27](https://iam0engr4ali.atlassian.net/browse/PNCRT-27) |
