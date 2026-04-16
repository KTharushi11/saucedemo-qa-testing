# Checkout Test Cases

---

### Test Case ID : TC014

### Test Title   : Verify user can initiate checkout process

### Type of Testing : Functional Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart

**Description:**
Verify that the user can initiate the checkout process from the cart page.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using valid credentials
3. Add a product to cart
4. Click on the cart icon
5. Click "Checkout" button

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* Product: Any item

**Expected Result:**

* User should be redirected to the checkout information page
* Checkout form (First Name, Last Name, Zip/Postal Code) should be displayed

**Postcondition:**

* User is on checkout information page

**Actual Result:**

* User was redirected to checkout information page
* Form fields were displayed correctly

**Status:**
Pass

**Notes:**
Checkout process initiates successfully

---

### Test Case ID : TC015

### Test Title   : Verify checkout form validation with empty fields

### Type of Testing : Validation Testing, Negative Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart
* User is on the checkout information page

**Description:**
Verify that the system displays appropriate validation messages when checkout form is submitted with empty fields.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using valid credentials
3. Add a product to cart
4. Click on the cart icon
5. Click "Checkout"
6. Leave First Name, Last Name, and Postal Code fields empty
7. Click "Continue" button

**Test Data:**

* First Name: (empty)
* Last Name: (empty)
* Postal Code: (empty)

**Expected Result:**

* User should not proceed to the next step
* System should display validation error message (eg: "First Name is required")
* User should remain on checkout information page

**Postcondition:**

* Checkout process is blocked

**Actual Result:**

* System displayed error message "Error: First Name is required"
* User remained on checkout information page

**Status:**
Pass

**Notes:**
Validation is working correctly for empty mandatory fields

---
