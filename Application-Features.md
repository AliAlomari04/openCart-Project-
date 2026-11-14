# Application Features

## 1. Detailed Feature Breakdown (Per FRS Information Architecture)

### 1.1 Global Header
Displayed across every page of the store, containing:
* **Store Logo:** Redirects the customer back to the Home Page.
* **Currency Block:** Dropdown allowing currency selection (`€ Euro`, `£ Pound Sterling`, `$ US Dollar`).
* **Top Links & Contact:** Displays company telephone number (`123456789`), `My Account` dropdown (`Register`, `Login`), `Wish List (0)`, `Shopping Cart`, and `Checkout`.
* **Search Box:** Keyword search input bar to search across product categories.
* **Shopping Cart Button:** Displays item count and total price (e.g., `0 item(s) - $0.00`); clicking opens a quick view with options to `View Cart` or `Checkout`.

### 1.2 The Top Menu 
* Displays parent product categories across all pages: `Desktops`, `Laptops & Notebooks`, `Components`, `Tablets`, `Software`, `Phones & PDAs`, `Cameras`, `MP3 Players`.
* **Hover Behavior:** Dragging the mouse over a parent category displays a dropdown menu of sub-categories (e.g., `PC`, `Mac`).
* **Click Behavior:** Clicking a parent category directs the user to the Category Product Listing page.

### 1.3 Home Page: Slideshow & Featured Products 
* **Slideshow:** Rotates product promotional banners automatically on the Home Page only; clicking a banner navigates to the featured product page.
* **Featured Products:** Highlights selected sample products (`MacBook`, `iPhone`, `Apple Cinema 30"`, `Canon EOS 5D`) showing image, title, description snippet, price (with `Ex Tax`), and action buttons (`Add to Cart`, `Add to Wish List`, `Compare this Product`).

### 1.4 Global Footer 
Located at the bottom of every page, organized into 4 columns:
* **Information:** `About Us`, `Delivery Information`, `Privacy Policy`, `Terms & Conditions`.
* **Customer Service:** `Contact Us`, `Returns`, `Site Map`.
* **Extras:** `Brands`, `Gift Certificates / Vouchers`, `Affiliates`, `Specials`.
* **My Account:** `My Account`, `Order History`, `Wish List`, `Newsletter`.

### 1.5 Product Detail Page 
* **Product Image:** Main image on the left with thumbnail alternate views underneath; clicking expands the image in a lightbox modal.
* **Product Details:** Displays Brand link, Product Code, Reward Points, Availability (`In Stock`), and Price (including `Ex Tax`).
* **Cart & Options:** Mandatory/optional product options (e.g., `Select` dropdown), Quantity (`Qty`) input, `Add to Cart` button, plus `Wish List` and `Compare` icons.
* **Rating & Sharing:** Star rating summary, `Write a review` link, and social media sharing buttons.
* **Information Tabs:** `Description` tab for detailed overview and `Reviews` tab for reading/submitting customer reviews.

### 1.6 Category Product Listings 
* **Access Paths:** Via Top Menu parent categories or the Left-Side Category Block.
* **Sub-Category Navigation:** `Refine Search` links at the top of the category page.
* **Display Controls:** Toggle between **List View** and **Grid View**, sort products via `Sort By` (`Default`, `Name`, `Price`, `Rating`, `Model`), and adjust page size via `Show` dropdown (`10` / `15` up to `100`).

### 1.7 Product Compare 
* Displays a side-by-side comparison table covering: `Product Name`, `Image`, `Price`, `Model`, `Brand`, `Availability`, `Rating`, `Summary`, `Weight`, and `Dimensions (L x W x H)`.
* Includes direct `Add to Cart` and `Remove` buttons per product, and a `Continue` button returning to the Home Page.

### 1.8 Shopping Cart Page
* **Cart Table Columns:** `Image`, `Product Name` (with selected options & reward points), `Model`, `Quantity` (with Update & Remove buttons), `Unit Price`, and `Total`.
* **Next Step Panels:** Collapsible accordions for `Estimate Shipping & Taxes`, `Use Coupon Code`, and `Use Gift Certificate`, alongside `Sub-Total`, `Eco Tax`, `VAT`, and `Total` calculations.
* **Navigation CTAs:** `Continue Shopping` (returns to Home Page) and `Checkout`.

### 1.9 Creating an Account & Logging In 
* **Path 1 — Via Checkout Step 1:** Selecting `Register Account` converts Step 2 into `Account & Billing Details`, requesting Personal Details (`First Name`, `Last Name`, `E-Mail`, `Telephone`), Shipping Address, and Password creation.
* **Path 2 — Via Header My Account -> Register:** Opens the standalone `Register Account` form (`First Name`, `Last Name`, `E-Mail`, `Telephone`, `Password`, `Password Confirm`, `Newsletter Subscribe Yes/No`, and `Privacy Policy` checkbox).
* **Returning Customer Login (My Account -> Login):** Allows authentication using `E-Mail Address` and `Password`, with a `Forgotten Password` recovery link.

### 1.10 Checkout & Order History 
* **6-Step Checkout Process:**
  1. **Step 1: Checkout Options:** Register Account, Guest Checkout, or Returning Customer Login.
  2. **Step 2: Billing Details:** Personal & address details; option to indicate delivery and billing details are the same.
  3. **Step 3: Delivery Details:** Skipped if same as billing; otherwise captures separate shipping address.
  4. **Step 4: Delivery Method:** Shipping method selection + Order comments box.
  5. **Step 5: Payment Method:** Payment method selection, order comments, and Terms & Conditions agreement.
  6. **Step 6: Confirm Order:** Final summary of product description, quantity, unit price, shipping rate, tax, and `Confirm Order` button.
* **Post-Order Verification:** Displays `'Your order has been placed!'` confirmation screen, and logs the transaction under `My Account >> Order History` (showing `Order ID`, `Date Added`, `Status: Pending`, `Payment/Shipping Address`, and item totals).

---

## 2. Static Testing Findings 
During the requirement analysis phase, the following documentation discrepancies were identified in `FRS(OpenCart).pdf` (v1.0):

1. **DOC-BUG-01 (Page 13 — Login Fields Mismatch):** The text under *Figure 14* states: *"Here, the customer has to enter their 'E-Mail'; 'Telephone' and 'Password' to Log in."* However, *Figure 14* and the live OpenCart Login page only require **E-Mail Address** and **Password** (no Telephone field exists on Login).
2. **DOC-BUG-02 (Page 8 vs. Page 9 — Show Limit Default):** Page 8 states that the `Show` dropdown changes product limits *"from 15 to 100"*, whereas *Figure 8* on Page 9 shows the default `Show` limit set to `10`.
3. **DOC-BUG-03 (Page 6 vs. Page 7 — Footer Link Naming):** Page 6 lists the footer link under Extras as `"Gift Vouchers"`, while *Figure 1* (Page 3) and *Figure 6* (Page 7) display the UI text as `"Gift Certificates"`.