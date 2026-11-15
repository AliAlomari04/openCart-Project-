# Test Scenarios 

| Document Information | Details |
| :--- | :--- |
| **Project Name** | OpenCart (Frontend) Manual QA Project |
| **Author** | Ali Alomari|
| **Reference Document** | OpenCart Functional Requirement Specification (FRS v1.0) |
| **Total Modules Covered** | 19 Functional Modules (`TS_001` – `TS_019`) |
| **Total Detailed Scenarios** | 118 Test Scenarios (Positive, Negative, Boundary, Integration, UI) |
| **Total Estimated Test Cases** | 349 Test Cases |

---

## 1. FRS Requirement Analysis & Scenario Design Approach
All test scenarios in this document are directly derived from the **OpenCart Project Functional Requirement Specification (FRS v1.0)** as the primary source of truth. Rather than relying solely on high-level module labels, this document implements a **Hybrid Scenario Architecture**:
* **Parent Module Mapping (`TS_001` – `TS_019`):** Maintains 100% traceability with the 19 functional storefront modules and the 349 planned test cases.
* **Detailed Condition Decomposition (`TS_00X_01+`):** Breaks down each FRS section into Positive (Happy Path), Negative (Validation & Error Handling), Boundary, Integration (End-to-End), and UI/Usability scenarios.

---

## 2. Module Summary & Traceability Matrix Overview

| Parent ID | Module Name | FRS Section Ref | Priority | Detailed Scenarios | Est. Test Cases |
| :---: | :--- | :---: | :---: | :---: | :---: |
| `TS_001` | Register Account | `FRS 4.1.12` | P0 (High) | 9 | 27 |
| `TS_002` | Login | `FRS 4.1.12` | P0 (High) | 8 | 23 |
| `TS_003` | Logout | `FRS 4.1.12` | P0 (High) | 6 | 11 |
| `TS_004` | Forgot Password | `FRS 4.1.12` | P2 (Low) | 7 | 25 |
| `TS_005` | Search | `FRS 4.1.3 / 4.1.9` | P1 (Medium) | 8 | 22 |
| `TS_006` | Product Compare | `FRS 4.1.10` | P2 (Low) | 8 | 24 |
| `TS_007` | Product Display Page (PDP) | `FRS 4.1.8` | P1 (Medium) | 9 | 37 |
| `TS_008` | Add to Cart | `FRS 4.1.6 / 4.1.8` | P0 (High) | 4 | 9 |
| `TS_009` | Wish List | `FRS 4.1.3 / 4.1.8` | P2 (Low) | 6 | 21 |
| `TS_010` | Shopping Cart | `FRS 4.1.11` | P0 (High) | 8 | 33 |
| `TS_011` | Home Page, Header & Footer | `FRS 4.1.1 – 4.1.7` | P1 (Medium) | 5 | 10 |
| `TS_012` | Checkout (6-Step Flow) | `FRS 4.1.13` | P0 (High) | 7 | 20 |
| `TS_013` | My Account | `FRS 4.1.12` | P2 (Low) | 4 | 9 |
| `TS_014` | Account Information | `FRS 4.1.12` | P3 (Low) | 5 | 13 |
| `TS_015` | Change Password | `FRS 4.1.12` | P3 (Low) | 5 | 13 |
| `TS_016` | Address Book | `FRS 4.1.12` | P3 (Low) | 6 | 21 |
| `TS_017` | Order History | `FRS 4.1.13` | P2 (Low) | 4 | 12 |
| `TS_018` | Order Information | `FRS 4.1.13` | P2 (Low) | 4 | 8 |
| `TS_019` | Product Returns | `FRS 4.1.7` | P3 (Low) | 5 | 11 |
| **TOTAL** | **19 Modules** | **FRS 4.1.1 – 4.1.13** | **P0 – P3** | **118** | **349** |

---

## 3. Detailed Test Scenarios by Module

### 3.1 `TS_001` — Register Account (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_001_01` | Positive | Verify registering a new account by providing only the mandatory fields (First Name, Last Name, E-Mail, Telephone, Password, Password Confirm, and Privacy Policy). | P0 (High) | 3 |
| `TS_001_02` | Positive | Verify registering a new account by providing all mandatory and optional fields (including Newsletter Yes/No subscription). | P0 (High) | 3 |
| `TS_001_03` | Positive | Verify navigating to the Register Account page from multiple entry points (Header 'My Account -> Register', Login Page 'New Customer -> Continue', Right Column link, and Checkout Step 1). | P1 (Medium) | 4 |
| `TS_001_04` | Negative | Verify appropriate field-level validation error messages when submitting the Register Account form with all mandatory fields left blank. | P0 (High) | 2 |
| `TS_001_05` | Negative | Verify that account registration fails with a warning banner when using an already registered E-Mail address. | P0 (High) | 2 |
| `TS_001_06` | Negative | Verify validation error when 'Password' and 'Password Confirm' fields do not match. | P0 (High) | 2 |
| `TS_001_07` | Negative | Verify field validation for invalid formats and boundary lengths on E-Mail, Telephone, First Name, Last Name, and Password. | P1 (Medium) | 6 |
| `TS_001_08` | Negative | Verify that registration is blocked with a warning banner when the 'Privacy Policy' checkbox is not selected. | P0 (High) | 2 |
| `TS_001_09` | UI / Usability | Verify UI elements, placeholders, mandatory red asterisks (*), password masking, breadcrumb navigation, and page title on the Register Account page. | P2 (Low) | 3 |

---

### 3.2 `TS_002` — Login (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_002_01` | Positive | Verify logging in with valid registered E-Mail Address and valid Password, including case-insensitivity for the E-Mail field. | P0 (High) | 3 |
| `TS_002_02` | Positive | Verify navigating to the Login page from multiple entry points (Header 'My Account -> Login', Right Column link, Register page link, and Checkout Step 1) and redirecting to Register via 'New Customer -> Continue'. | P1 (Medium) | 4 |
| `TS_002_03` | Positive | Verify that clicking the 'Forgotten Password' link redirects the user to the 'Forgot Your Password?' recovery page. | P1 (Medium) | 2 |
| `TS_002_04` | Negative | Verify login failure and warning message when providing invalid credentials (unregistered email, wrong password, or both invalid). | P0 (High) | 4 |
| `TS_002_05` | Negative | Verify login failure when leaving E-Mail Address, Password, or both fields blank, or submitting whitespace-only characters. | P0 (High) | 4 |
| `TS_002_06` | Negative | Verify password case-sensitivity (rejecting uppercase/lowercase mismatch) and account lockout warning after exceeding maximum failed login attempts. | P1 (Medium) | 3 |
| `TS_002_07` | Integration / E2E | Verify session persistence after logging in (Checking 'My Account' dashboard redirect, browser Back button behavior, and logging out). | P1 (Medium) | 2 |
| `TS_002_08` | UI / Usability | Verify UI elements, placeholders, password masking, Tab key navigation, and Screen-Reader accessibility labels/error announcements on the Login page. | P2 (Low) | 1 |

---

### 3.3 `TS_003` — Logout (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_003_01` | Positive | Verify logging out via both available entry points (Header 'My Account -> Logout' dropdown and Right Column 'Logout' link), displaying the 'Account Logout' confirmation page, and redirecting to the Home Page upon clicking 'Continue'. | P0 (High) | 3 |
| `TS_003_02` | Positive | Verify that the 'Logout' option is hidden for guest users (before login) and disappears from both the Header 'My Account' dropdown and Right Column immediately after logging out. | P1 (Medium) | 2 |
| `TS_003_03` | Negative | Verify that a logged-out user cannot access protected 'My Account' pages via the browser 'Back' button or direct URL navigation, and is redirected to the Login page. | P0 (High) | 2 |
| `TS_003_04` | Integration / E2E | Verify session invalidation across multiple open browser tabs (logging out in Tab A invalidates the active session in Tab B upon refresh/action) and session cookie clearance. | P1 (Medium) | 2 |
| `TS_003_05` | Integration / E2E | Verify Shopping Cart state upon logging out and logging back in (saved cart items are cleared from the guest view after logout and restored upon re-login). | P1 (Medium) | 1 |
| `TS_003_06` | UI / Usability | Verify UI layout, breadcrumb navigation, page title, and visibility of the 'Logout' option and 'Account Logout' confirmation screen. | P2 (Low) | 1 |

---

### 3.4 `TS_004` — Forgot Password (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_004_01` | Positive | Verify requesting a password reset with a valid registered E-Mail Address, redirecting to the Login page with a confirmation banner ('An email with a confirmation link has been sent...'). | P1 (Medium) | 3 |
| `TS_004_02` | Positive | Verify navigating to the 'Forgot Your Password?' page from multiple entry points (Login page link and Right Column link) and returning to the Login page via the 'Back' button. | P2 (Low) | 4 |
| `TS_004_03` | Positive | Verify completing the password reset flow via the email confirmation link and logging in successfully with the newly set password. | P1 (Medium) | 4 |
| `TS_004_04` | Negative | Verify error message when submitting a non-registered E-Mail Address, an invalid email format, or leaving the E-Mail Address field blank. | P1 (Medium) | 5 |
| `TS_004_05` | Negative | Verify that the user cannot log in using the old password after successfully resetting the password. | P1 (Medium) | 2 |
| `TS_004_06` | Negative | Verify password reset failure when using an expired/invalid reset token link, or when the new 'Password' and 'Password Confirm' fields do not match or violate length limits. | P2 (Low) | 4 |
| `TS_004_07` | UI / Usability | Verify UI elements, instruction text on top, mandatory asterisk (*), 'E-Mail Address' placeholder, breadcrumb navigation, and page title on the Forgot Password page. | P2 (Low) | 3 |

---

### 3.5 `TS_005` — Search (`FRS 4.1.3 / 4.1.9`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_005_01` | Positive | Verify searching for existing products using full product names (single and multiple matching results), partial keywords, and triggering search via both the Search icon button and the 'Enter' key. | P0 (High) | 4 |
| `TS_005_02` | Positive | Verify search behavior for logged-in users vs. guest users, case-insensitivity (uppercase/lowercase), and keywords with leading/trailing spaces. | P1 (Medium) | 3 |
| `TS_005_03` | Positive | Verify advanced search criteria on the Search page: filtering by Category, enabling 'Search in subcategories', and enabling 'Search in product descriptions'. | P1 (Medium) | 3 |
| `TS_005_04` | Positive | Verify Search Results display controls: toggling between List and Grid views, sorting results via 'Sort By' (Name, Price, Rating, Model), and changing item count via 'Show' dropdown. | P1 (Medium) | 3 |
| `TS_005_05` | Negative | Verify searching for a non-existing product name, misspelled product name (typo), or multi-word product name without spaces displays 'There is no product that matches the search criteria.'. | P1 (Medium) | 3 |
| `TS_005_06` | Negative | Verify searching with an empty Search box, whitespace-only input, or special characters/SQL-like symbols without crashing the application. | P1 (Medium) | 3 |
| `TS_005_07` | Integration / E2E | Verify end-to-end navigation from Search Results: clicking 'Product Compare' link, adding a searched product directly to Cart/Wish List, or opening its Product Display Page. | P1 (Medium) | 2 |
| `TS_005_08` | UI / Usability | Verify Search bar placeholder ('Search'), breadcrumb navigation, page heading ('Search - [keyword]'), and layout consistency across pages. | P2 (Low) | 1 |

---

### 3.6 `TS_006` — Product Compare (`FRS 4.1.10`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_006_01` | Positive | Verify adding products to comparison from different pages (Product Display Page, Featured section, Search Results, and Category List/Grid views) and confirming the green success banner with the 'product comparison' link. | P1 (Medium) | 5 |
| `TS_006_02` | Positive | Verify comparing 2 or more products from the same category and from different categories, ensuring accurate side-by-side display of all details (Product Name, Image, Price, Model, Brand, Availability, Rating, Summary, Weight, Dimensions). | P1 (Medium) | 4 |
| `TS_006_03` | Boundary | Verify Product Compare capacity limits: viewing 1, 2, 3, and up to the maximum of 4 products, and verifying that adding a 5th product automatically replaces the oldest compared product. | P2 (Low) | 4 |
| `TS_006_04` | Positive | Verify action buttons inside the Product Comparison table: clicking 'Add to Cart' adds the specific product to the Shopping Cart, and clicking 'Remove' deletes the product column and updates the table. | P1 (Medium) | 4 |
| `TS_006_05` | Positive | Verify that clicking the 'Continue' button on the Product Comparison page redirects the user back to the Home Page without adding unselected products to the cart. | P2 (Low) | 2 |
| `TS_006_06` | Negative | Verify empty comparison state when navigating to 'Product Compare (0)' without selecting any products, or after removing all products from the comparison table ('You have not chosen any products to compare.'). | P2 (Low) | 2 |
| `TS_006_07` | Negative | Verify that clicking 'Compare this Product' multiple times on the exact same product does not create duplicate columns in the Product Comparison table. | P2 (Low) | 1 |
| `TS_006_08` | UI / Usability | Verify UI elements, tooltip text ('Compare this Product'), dynamic counter update on the 'Product Compare (X)' link, breadcrumb navigation, and page title. | P3 (Low) | 2 |

---

### 3.7 `TS_007` — Product Display Page (`FRS 4.1.8`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_007_01` | Positive | Verify navigating to the Product Display Page (PDP) by clicking on a product's image or name from various sections (Home Featured, Search Results, Category Listing, Product Compare, Shopping Cart) and displaying accurate product details (Title, Brand link, Product Code, Reward Points, Availability status, Price, and Ex Tax price). | P0 (High) | 5 |
| `TS_007_02` | Positive | Verify Product Image gallery and Lightbox modal: clicking the main image or alternate thumbnail images expands the image in a modal window with working Next/Previous arrows, image counter, and close ('X' / Esc) functionality. | P1 (Medium) | 4 |
| `TS_007_03` | Positive | Verify adding a product to the cart from the PDP with default quantity ('1'), custom positive quantities ('Qty > 1'), and valid 'Available Options' (e.g., dropdown color/size selection), ensuring product details match in the cart. | P0 (High) | 4 |
| `TS_007_04` | Positive | Verify 'Add to Wish List' and 'Compare this Product' buttons on the PDP, along with switching between 'Description', 'Specification' (when applicable), and 'Reviews' tabs. | P1 (Medium) | 4 |
| `TS_007_05` | Positive | Verify submitting a valid product review under the 'Reviews' tab (or via 'Write a review' link) with valid Name, Review text (>= 25 chars), and Star Rating (1–5), confirming the approval notification banner. | P1 (Medium) | 5 |
| `TS_007_06` | Negative | Verify validation errors when clicking 'Add to Cart' without selecting mandatory 'Available Options' (e.g., '* Select' dropdown on Canon EOS 5D) or when entering invalid quantities (0, negative numbers, blank, or non-numeric characters in 'Qty'). | P0 (High) | 5 |
| `TS_007_07` | Negative | Verify stock and minimum order quantity constraints: adding a quantity exceeding available stock (triggers '***' out-of-stock warning in Shopping Cart) or adding less than the required Minimum Quantity for restricted products (e.g., Apple Cinema 30"). | P1 (Medium) | 5 |
| `TS_007_08` | Negative | Verify validation errors when submitting a product review with blank fields, review text shorter than 25 characters or exceeding 1000 characters, or without selecting a star rating. | P2 (Low) | 3 |
| `TS_007_09` | UI / Usability | Verify UI alignment, breadcrumb navigation, page title, social media sharing links, average star rating display, and related products section (if present) on the PDP. | P2 (Low) | 2 |

---

### 3.8 `TS_008` — Add to Cart (`FRS 4.1.6 / 4.1.8`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_008_01` | Positive | Verify adding a product to the Shopping Cart from all available store locations (Home Page Featured section, Product Display Page, Search Results, Category List/Grid views, Wish List, and Product Comparison page). | P0 (High) | 4 |
| `TS_008_02` | Positive | Verify that clicking 'Add to Cart' displays the green success notification banner ('Success: You have added [Product] to your shopping cart!') and dynamically increments the Header Cart button item count and total price. | P0 (High) | 2 |
| `TS_008_03` | Positive | Verify adding a product that requires mandatory options (e.g., Canon EOS 5D or Apple Cinema 30") from Category/Search/Featured listings automatically redirects the user to the Product Display Page to complete required options. | P1 (Medium) | 2 |
| `TS_008_04` | Positive | Verify that adding the same product multiple times increments its existing quantity in the cart rather than creating duplicate rows. | P1 (Medium) | 1 |

---

### 3.9 `TS_009` — Wish List (`FRS 4.1.3 / 4.1.8`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_009_01` | Positive | Verify adding products to the Wish List as a logged-in user from various pages (PDP, Home Featured, Search Results, Category Listings) and accessing the 'My Wish List' page via the success banner link, Header 'Wish List (X)' link, or Footer/My Account links. | P2 (Low) | 5 |
| `TS_009_02` | Positive | Verify My Wish List table details (Image, Product Name, Model, Stock status, Unit Price) and action buttons: clicking the 'Add to Cart' icon adds the item to the Shopping Cart, and clicking the red 'Remove' icon deletes it from the Wish List. | P2 (Low) | 5 |
| `TS_009_03` | Negative | Verify guest user behavior when clicking 'Add to Wish List' (displays alert: 'You must login or create an account to save [Product] to your wish list!') and redirects to Login when clicking Header 'Wish List'. | P2 (Low) | 4 |
| `TS_009_04` | Negative | Verify duplicate handling and empty state: adding the same product twice to the Wish List does not duplicate rows, and removing all items displays 'Your wish list is empty.' with a working 'Continue' button. | P2 (Low) | 4 |
| `TS_009_05` | Integration / E2E | Verify that a product clicked for Wish List by a guest user before logging in is persisted and automatically added to their Wish List upon successful Login. | P2 (Low) | 2 |
| `TS_009_06` | UI / Usability | Verify UI elements, dynamic counter update on Header 'Wish List (X)', breadcrumb navigation, and page title on the My Wish List page. | P3 (Low) | 1 |

---

### 3.10 `TS_010` — Shopping Cart (`FRS 4.1.11`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_010_01` | Positive | Verify navigating to the Shopping Cart page via the Header 'Shopping Cart' link, the black Cart dropdown 'View Cart' button, or the green success banner link, and verifying all table columns (Image, Product Name, Model, Quantity, Unit Price, Total) and total weight in heading. | P0 (High) | 5 |
| `TS_010_02` | Positive | Verify updating product quantity to a valid positive number and clicking the blue 'Update' button recalculates Line Total, Sub-Total, Eco Tax, VAT, and Grand Total accurately, and clicking 'Remove' deletes the item from the cart. | P0 (High) | 6 |
| `TS_010_03` | Positive | Verify 'Use Coupon Code' and 'Use Gift Certificate' collapsible panels with valid codes, ensuring the discount is applied accurately to the order total. | P1 (Medium) | 5 |
| `TS_010_04` | Positive | Verify 'Estimate Shipping & Taxes' accordion by selecting valid Country, Region/State, and Post Code, clicking 'Get Quotes', selecting a shipping rate modal option, and applying shipping cost to the cart total. | P1 (Medium) | 5 |
| `TS_010_05` | Positive | Verify navigation CTAs on the Shopping Cart page: clicking 'Continue Shopping' redirects to the Home Page, and clicking 'Checkout' redirects to the 6-Step Checkout page. | P0 (High) | 3 |
| `TS_010_06` | Negative | Verify updating quantity with 0, negative numbers, blank, or non-numeric characters (0/negative removes item or shows error), or updating to a quantity exceeding available stock (displays '***' out-of-stock warning banner). | P0 (High) | 4 |
| `TS_010_07` | Negative | Verify warning messages when submitting empty, invalid, or expired Coupon Codes / Gift Certificates, or leaving mandatory Country/Region/Post Code fields blank in 'Estimate Shipping & Taxes'. | P1 (Medium) | 3 |
| `TS_010_08` | UI / Usability | Verify empty Shopping Cart state ('Your shopping cart is empty!'), Header Cart dropdown quick-remove ('X') button, breadcrumb navigation, and page title. | P2 (Low) | 2 |

---

### 3.11 `TS_011` — Home Page, Header & Footer (`FRS 4.1.1 – 4.1.7`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_011_01` | Positive | Verify Store Logo redirection to the Home Page from any store page, and verify Header Top Links ('Telephone', 'My Account', 'Wish List', 'Shopping Cart', 'Checkout'). | P1 (Medium) | 2 |
| `TS_011_02` | Positive | Verify Currency Switcher dropdown in the Header ('€ Euro', '£ Pound Sterling', '$ US Dollar'), ensuring product prices and cart totals dynamically update to the selected currency symbol and rate across all pages. | P1 (Medium) | 2 |
| `TS_011_03` | Positive | Verify Top Menu navigation: hovering over parent categories displays sub-category dropdowns (e.g., Desktops -> PC, Mac), and clicking a category or 'Show All' opens the Category Product Listing page with 'Refine Search' and Left Category Block. | P1 (Medium) | 2 |
| `TS_011_04` | Positive | Verify Home Page Hero Slideshow auto-rotation, manual Next/Previous arrows, banner click redirection, Brand logo carousel, and 'Featured' products grid display. | P2 (Low) | 2 |
| `TS_011_05` | Positive | Verify Global Footer links across all 4 sections ('Information', 'Customer Service' including Contact Us & Site Map, 'Extras' including Brands & Specials, and 'My Account'). | P2 (Low) | 2 |

---

### 3.12 `TS_012` — Checkout (`FRS 4.1.13`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_012_01` | Positive | Verify end-to-end 6-Step Checkout as a Logged-in Customer using an existing address or adding a new Billing/Delivery address, selecting Delivery Method, accepting Payment Method Terms & Conditions, and clicking 'Confirm Order' to reach 'Your order has been placed!'. | P0 (High) | 4 |
| `TS_012_02` | Positive | Verify Step 1 Checkout Options for unauthenticated users: completing checkout via 'Register Account' (Step 2 becomes Account & Billing Details) or via 'Guest Checkout' (when applicable), or logging in directly as a 'Returning Customer'. | P0 (High) | 4 |
| `TS_012_03` | Positive | Verify Step 2 & Step 3 address handling: checking 'My delivery and billing addresses are the same' skips/syncs Delivery Details, while unchecking it allows entering a separate shipping address. | P1 (Medium) | 3 |
| `TS_012_04` | Positive | Verify Step 4 (Delivery Method), Step 5 (Payment Method), and Step 6 (Confirm Order): adding order comments, verifying accurate item summary/shipping rate/tax breakdown in Step 6, and redirecting to Home Page upon clicking 'Continue' on the Order Success page. | P0 (High) | 3 |
| `TS_012_05` | Negative | Verify field-level validation errors in Step 2 (Billing Details) and Step 3 (Delivery Details) when leaving mandatory fields (First Name, Last Name, Address 1, City, Post Code, Country, Region/State) blank or providing invalid formats. | P0 (High) | 3 |
| `TS_012_06` | Negative | Verify that checkout progression is blocked with a warning banner when the 'Terms & Conditions' checkbox is not checked in Step 5 (Payment Method), or when attempting to checkout with an empty cart or out-of-stock ('***') product. | P0 (High) | 2 |
| `TS_012_07` | UI / Usability | Verify accordion step transitions, ability to re-open and edit previous completed Checkout steps (Steps 1–5) before confirming the order, breadcrumb navigation, and page title. | P2 (Low) | 1 |

---

### 3.13 `TS_013` — My Account (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_013_01` | Positive | Verify navigating to the 'My Account' dashboard after logging in, via the Header 'My Account' dropdown, Right Column link, Footer 'My Account' link, or 'Account' breadcrumb. | P2 (Low) | 3 |
| `TS_013_02` | Positive | Verify all main dashboard section headings ('My Account', 'My Orders', 'My Affiliate Account', 'Newsletter') and right-hand navigation links redirect to their respective sub-pages. | P2 (Low) | 3 |
| `TS_013_03` | Negative | Verify that unauthenticated guest users attempting to access 'My Account' via Footer link or direct URL are redirected to the Login page. | P2 (Low) | 2 |
| `TS_013_04` | UI / Usability | Verify UI layout, breadcrumb navigation, and page title ('My Account') on the account dashboard. | P3 (Low) | 1 |

---

### 3.14 `TS_014` — Account Information (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_014_01` | Positive | Verify navigating to 'My Account Information' via 'Edit your account information' link or Right Column 'Edit Account', confirming existing First Name, Last Name, E-Mail, and Telephone are pre-populated accurately. | P3 (Low) | 3 |
| `TS_014_02` | Positive | Verify updating First Name, Last Name, E-Mail, and Telephone with valid data and clicking 'Continue' saves changes and displays 'Success: Your account has been successfully updated.'. | P3 (Low) | 3 |
| `TS_014_03` | Positive | Verify that clicking the 'Back' button on the 'My Account Information' page discards unsaved edits and returns to the My Account dashboard. | P3 (Low) | 2 |
| `TS_014_04` | Negative | Verify validation error messages when clearing mandatory fields (First Name, Last Name, E-Mail, Telephone), entering invalid email/phone formats, or updating E-Mail to an address already registered to another user. | P3 (Low) | 4 |
| `TS_014_05` | UI / Usability | Verify UI elements, mandatory red asterisks (*), placeholders, breadcrumb navigation, and page title on the 'My Account Information' page. | P3 (Low) | 1 |

---

### 3.15 `TS_015` — Change Password (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_015_01` | Positive | Verify navigating to the 'Change Password' page via 'Change your password' link or Right Column 'Password' link, entering matching valid 'Password' and 'Password Confirm', and verifying the success banner ('Success: Your password has been successfully updated.'). | P3 (Low) | 3 |
| `TS_015_02` | Positive | Verify logging out and logging back in using the newly updated password, and verifying that the 'Back' button returns to My Account without changing the password. | P3 (Low) | 3 |
| `TS_015_03` | Negative | Verify validation errors when leaving 'Password' or 'Password Confirm' blank, or when 'Password' and 'Password Confirm' do not match ('Password confirmation does not match password!'). | P3 (Low) | 3 |
| `TS_015_04` | Negative | Verify boundary validation on the new password (fewer than 4 characters or greater than 20 characters) and verify that logging in with the old password fails after a password change. | P3 (Low) | 3 |
| `TS_015_05` | UI / Usability | Verify password masking (bullet/asterisk characters), mandatory red asterisks (*), placeholders, breadcrumb navigation, and page title on the Change Password page. | P3 (Low) | 1 |

---

### 3.16 `TS_016` — Address Book (`FRS 4.1.12`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_016_01` | Positive | Verify navigating to 'Address Book Entries' via My Account or Right Column 'Address Book', and adding a new address via 'New Address' with valid mandatory and optional fields. | P3 (Low) | 5 |
| `TS_016_02` | Positive | Verify editing an existing address via 'Edit', changing the 'Default Address' radio button (Yes/No), and confirming the updated details in the Address Book list. | P3 (Low) | 4 |
| `TS_016_03` | Positive | Verify deleting a non-default secondary address via the 'Delete' button and confirming the 'Your address has been successfully deleted' message. | P3 (Low) | 3 |
| `TS_016_04` | Negative | Verify field-level validation errors when submitting the Add/Edit Address form with blank mandatory fields (First Name, Last Name, Address 1, City, Post Code, Country, Region/State). | P3 (Low) | 5 |
| `TS_016_05` | Negative | Verify that OpenCart prevents deleting the Default Address or the only remaining address in the account ('Warning: You can not delete your default address!' / 'Warning: You must have at least one address!'). | P3 (Low) | 3 |
| `TS_016_06` | UI / Usability | Verify dynamic Region/State dropdown loading based on selected Country, breadcrumb navigation, 'Back' button, and page title on Address Book pages. | P3 (Low) | 1 |

---

### 3.17 `TS_017` — Order History (`FRS 4.1.13`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_017_01` | Positive | Verify navigating to 'Order History' via My Account, Right Column 'Order History', Footer link, or Order Success page link, and verifying the orders table columns (Order ID, Customer, No. of Products, Status, Total, Date Added). | P2 (Low) | 4 |
| `TS_017_02` | Positive | Verify that newly placed orders appear at the top of the Order History table with accurate Order ID, 'Pending' status, item count, and total, and clicking the 'View' (eye) icon opens the Order Information page. | P2 (Low) | 4 |
| `TS_017_03` | Negative | Verify empty state message ('You have not made any previous orders!') for a newly registered account with 0 orders, and verify guest users are redirected to Login when accessing Order History. | P3 (Low) | 2 |
| `TS_017_04` | UI / Usability | Verify 'Continue' button redirection to My Account, pagination for multiple orders, breadcrumb navigation, and page title on the Order History page. | P3 (Low) | 2 |

---

### 3.18 `TS_018` — Order Information (`FRS 4.1.13`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_018_01` | Positive | Verify 'Order Information' page details: Order ID, Date Added, Payment Method, Shipping Method, Payment Address, Shipping Address, Product table (Name, Model, Quantity, Price, Total), Sub-Total, Shipping Rate, Grand Total, and Order History status table. | P2 (Low) | 3 |
| `TS_018_02` | Positive | Verify clicking the blue 'Reorder' (shopping cart) icon on an order line item adds that product back to the Shopping Cart with a green confirmation banner. | P2 (Low) | 2 |
| `TS_018_03` | Positive | Verify clicking the red 'Return' (arrow) icon redirects the user to the 'Product Returns' form pre-populated with the selected Order ID and Product details, and clicking 'Continue' returns to Order History. | P3 (Low) | 2 |
| `TS_018_04` | UI / Usability | Verify UI layout, address formatting, breadcrumb navigation ('Account > Order History > Order Information'), and page title. | P3 (Low) | 1 |

---

### 3.19 `TS_019` — Product Returns (`FRS 4.1.7`)

| Scenario ID | Type | Test Scenario Description (What to Test) | Priority | Est. TCs |
| :---: | :---: | :--- | :---: | :---: |
| `TS_019_01` | Positive | Verify submitting a valid Product Return request (via Order Information 'Return' icon or Footer 'Returns' link) with valid Order Information, Product Information, 'Reason for Return' radio option, 'Product is opened' (Yes/No), and Faulty details, reaching the Return confirmation screen. | P3 (Low) | 3 |
| `TS_019_02` | Positive | Verify viewing submitted return requests under 'My Account -> View your return requests' (or Right Column 'Returns') and clicking 'View' to inspect Return Information details (Return ID, Status, Date Added, Product, Reason, Action). | P3 (Low) | 3 |
| `TS_019_03` | Negative | Verify validation error messages on the Product Returns form when leaving mandatory fields blank (First Name, Last Name, E-Mail, Telephone, Order ID, Product Name, Product Code, or Reason for Return radio selection). | P3 (Low) | 3 |
| `TS_019_04` | Negative | Verify empty state ('You have not made any previous returns!') for users with no return requests, and verify 'Back' button navigation on the Product Returns form. | P3 (Low) | 1 |
| `TS_019_05` | UI / Usability | Verify date picker widget for 'Order Date', mandatory red asterisks (*), placeholders, breadcrumb navigation, and page title on Product Returns pages. | P3 (Low) | 1 |
