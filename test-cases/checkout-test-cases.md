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

### Test Case ID : TC016

### Test Title   : Verify checkout with valid details

### Type of Testing : Functional Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart

**Description:**
Verify that the user can successfully complete the checkout process using valid information.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using username "standard_user" and password "secret_sauce"
3. Add a product to the cart
4. Click on the cart icon
5. Click "Checkout"
6. Enter valid details:

   * First Name: aaa
   * Last Name: bbb
   * Zip/Postal Code: 12345
7. Click "Continue"
8. Click "Finish"

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* First Name: aaa
* Last Name: bbb
* Zip/Postal Code: 12345

**Expected Result:**

* User should be redirected to the checkout overview page after entering details
* User should be able to complete the order successfully
* A confirmation message indicating successful order placement should be displayed

**Postcondition:**

* Order is successfully placed
* Cart is cleared

**Actual Result:**

* User was redirected to checkout overview page
* Order completed successfully
* Confirmation message "Thank you for your order!" displayed
* Cart was cleared

**Status:**
Pass

**Notes:**
Checkout process works correctly with valid inputs and completes the purchase successfully

---
