# OpenCart (Frontend) Manual QA Project

## 1. Project Description
**OpenCart** is a free, open-source e-commerce platform designed for online merchants to build and customize online stores. This project focuses on testing the **OpenCart Default Storefront (Frontend)**, which defines how customers view, navigate, and interact with the store .. from browsing product categories and comparing specifications to managing the shopping cart and completing the 6-step checkout process.

* **Project Name:** OpenCart (Frontend)
* **Domain:** E-Commerce / Online Retail
* **Application Under Test (AUT):** `https://demo.opencart.com`
* **Technical Stack (Per FRS):** PHP (5.4+), JavaScript, MySQL Database, Apache Web Server

---

## 2. Project Objectives
* Analyze the **Functional Requirement Specification (FRS)** and perform static requirement validation prior to test design.
* Verify the end-to-end customer purchase flow and all 13 frontend modules defined in the FRS Information Architecture.
* Design and execute comprehensive Test Scenarios and Test Cases covering positive, negative, and boundary conditions.
* Log, prioritize, and track defects using **Jira / Xray** and structured Excel templates, followed by Re-testing and Regression testing.

---

## 3. Target Users
1. **Guest Customers (Unregistered Visitors):** Users who browse categories, search and compare products, add items to the shopping cart, and either register an account or use Guest Checkout.
2. **Registered / Returning Customers:** Users who log in via their credentials to shop faster, manage their Wish List and Address Book, and track their orders via Order History.
3. **Shop Owners / Web Developers (Out of Scope for Frontend Execution):** Merchants configuring the store backend and product catalog.

---

## 4. Core End-to-End Customer Flow
> **Open Storefront** ➔ **Register / Login** (via Header or Checkout) ➔ **Select Product(s)** (Search / Category / Featured) ➔ **Add to Cart** ➔ **Shopping Cart Page** (Qty / Coupons / Taxes) ➔ **6-Step Checkout** ➔ **Confirm Order** ➔ **Order History**

---

## 5. Project Scope

### 5.1 In Scope (Frontend Modules)
1. **Navigation & Home Page:** Layout, Slideshow Banners, Featured Products.
2. **Global Header:** Store Logo, Currency Block, Search Box, Shopping Cart Dropdown, Top Links, Telephone, My Account Dropdown.
3. **The Top Menu:** Parent Categories & Hover Sub-Category Dropdowns.
4. **Global Footer:** Information, Customer Service, Extras, My Account Links.
5. **Product Detail Page (PDP):** Image Viewer, Details, Available Options/Qty, Cart/Wishlist/Compare CTAs, Rating/Sharing, Description & Review Tabs.
6. **Category Product Listings:** Left Category Block, Refine Search, List/Grid View, Sort By, Show Limit (15–100).
7. **Product Compare:** Specification comparison matrix, Add to Cart, Remove.
8. **Shopping Cart Page:** Item overview, Quantity update/removal, Estimate Shipping & Taxes, Coupon Code, Gift Certificate.
9. **Account Creation & Authentication:** Register (via Checkout Step 1 or Header My Account), Returning Customer Login, Forgotten Password, Logout.
10. **Checkout & Order History:** 6-Step Checkout workflow, Order Placed confirmation, My Account -> Order History & Downloads.

### 5.2 Out of Scope
* **Backend Admin Panel:** Store administration, inventory setup, and CMS management.
* **Non-Functional & White-Box Testing:** Performance/Load testing, Database testing, API testing, and Test Automation.
* **Future Enhancements:** Any feature added outside Version 1.0 of the FRS.
