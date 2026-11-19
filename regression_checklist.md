# Regression Testing Checklist – OpenCart 4.x (`demo.opencart.com`)

**Project:** OpenCart 4.x E-Commerce Storefront 
**Environment:** `https://demo.opencart.com`  
**Purpose:** Smoke & Regression verification checklist to validate core storefront workflows and critical validations after any build update or bug fix.

---

## 🔴 High Priority (`P1` – Core Business & Purchase Flow)

| ID | Module | Regression Check (Action & Expected Result) | Status |
| :--- | :--- | :--- | :---: |
| **REG-01** | **Registration** | Register a new account using valid mandatory fields and accept Privacy Policy; verify account creation confirmation page is displayed. | ⬜ |
| **REG-02** | **Login** | Log in with a valid registered email and password; verify redirection to the **My Account** dashboard. | ⬜ |
| **REG-03** | **Logout** | Log out from an active session and click **Continue**; verify redirection to the Home page. | ⬜ |
| **REG-04** | **Search** | Search for an existing product using its full name; verify matching product card(s) are displayed in results. | ⬜ |
| **REG-05** | **Product (PDP)** | Navigate to a Product Display Page (PDP); verify product title, price, availability, images, and description render properly. | ⬜ |
| **REG-06** | **Product (PDP)** | Click **Add to Cart** on a product with required options without selecting them; verify field-level validation error is triggered. | ⬜ |
| **REG-07** | **Cart** | Add an available product to the cart, update its quantity on the Shopping Cart page, and verify the cart badge, subtotal, and grand total recalculate accurately. | ⬜ |
| **REG-08** | **Cart** | Remove an item from the Shopping Cart; verify the grand total updates or the empty cart message is displayed. | ⬜ |
| **REG-09** | **Checkout** | Complete the end-to-end 6-step checkout flow as a logged-in customer; verify the order confirmation page appears. | ⬜ |
| **REG-10** | **Checkout** | Attempt to proceed to checkout with an out-of-stock (`***`) product in the cart; verify checkout is blocked with a warning banner. | ⬜ |

---

## 🟡 Medium Priority (`P2` – Negative Validations, Boundaries & Session Security)

| ID | Module | Regression Check (Action & Expected Result) | Status |
| :--- | :--- | :--- | :---: |
| **REG-11** | **Registration** | Submit the registration form with an invalid email format; verify submission is blocked with a field-level validation error. | ⬜ |
| **REG-12** | **Login** | Attempt to log in with a non-existent email or incorrect password; verify login fails and a warning banner is displayed. | ⬜ |
| **REG-13** | **Security / Session** | After logging out, attempt to access protected **My Account** pages via browser Back button or direct URL; verify redirection to the Login page. | ⬜ |
| **REG-14** | **Search** | Search for a non-existent or misspelled keyword; verify *"There is no product that matches the search criteria"* message is displayed. | ⬜ |
| **REG-15** | **Product (PDP)** | Enter `0` (`Min - 1`) in the PDP Quantity input and click **Add to Cart**; verify lower boundary validation prevents adding zero quantity. | ⬜ |

---

## 🟢 Low Priority (`P3` – Secondary Navigation & Access Points)

| ID | Module | Regression Check (Action & Expected Result) | Status |
| :--- | :--- | :--- | :---: |
| **REG-16** | **Account** | Verify logged-in users can navigate to **My Account** via Header dropdown, Right Column menu, Footer link, and Breadcrumb. | ⬜ |
| **REG-17** | **Account** | Verify unauthenticated guest users clicking **My Account** in the Footer are redirected to the Login page. | ⬜ |
