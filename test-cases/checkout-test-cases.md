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
6. Leave First Name, Last Name, and Zip/Postal Code fields empty
7. Click "Continue" button

**Test Data:**

* First Name: (empty)
* Last Name: (empty)
* Zip/Postal Code: (empty)

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

### Test Case ID : TC017

### Test Title   : Verify checkout with missing required field

### Type of Testing : Validation Testing, Negative Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart
* User is on the checkout information page

**Description:**
Verify that the system displays appropriate validation message when one of the required fields is missing.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using username "standard_user" and password "secret_sauce"
3. Add a product to the cart
4. Click on the cart icon
5. Click "Checkout"
6. Enter First Name: aaa
7. Leave Last Name empty
8. Enter Zip/Postal Code: 12345
9. Click "Continue"

**Test Data:**

* First Name: aaa
* Last Name: (empty)
* Zip/Postal Code: 12345

**Expected Result:**

* User should not proceed to the next step
* System should display validation error message indicating that Last Name is required
* User should remain on the checkout information page

**Postcondition:**

* Checkout process is blocked

**Actual Result:**

* System displayed error message "Error: Last Name is required"
* User remained on checkout information page

**Status:**
Pass

**Notes:**
Validation works correctly for missing required fields

---

### Test Case ID : TC018

### Test Title   : Verify checkout with invalid postal code format

### Type of Testing : Validation Testing, Negative Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart
* User is on the checkout information page

**Description:**
Verify how the system behaves when an invalid postal code format is entered during checkout.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using username "standard_user" and password "secret_sauce"
3. Add a product to the cart
4. Click on the cart icon
5. Click "Checkout"
6. Enter First Name: aaa
7. Enter Last Name: bbb
8. Enter invalid Zip/Postal Code: abc@123
9. Click "Continue"

**Test Data:**

* First Name: aaa
* Last Name: bbb
* Zip/Postal Code: abc@123

**Expected Result:**

* System should validate the postal code format if validation is implemented
* If validation exists, user should not be allowed to proceed and an error message should be displayed
* If validation is not implemented, system may accept the input and allow the user to proceed

**Postcondition:**

* Checkout proceeds based on system validation rules

**Actual Result:**

* System accepted the input and allowed user to proceed to the next step

**Status:**
Pass

**Notes:**
No validation is implemented for postal code format. This can be considered as a potential improvement for better data validation.

---

### Test Case ID : TC019

### Test Title   : Verify canceling checkout process navigates user back to cart

### Type of Testing : Functional Testing, UI Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart
* User is on the checkout information page

**Description:**
Verify that the user can cancel the checkout process and return to the cart page without losing cart items.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using username "standard_user" and password "secret_sauce"
3. Add a product to the cart
4. Click on the cart icon
5. Click "Checkout"
6. Click "Cancel" button

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* Product: Any item

**Expected Result:**

* User should be redirected back to the cart page
* Previously added product(s) should still be present in the cart
* Cart badge should remain unchanged

**Postcondition:**

* Cart remains intact
* Checkout process is canceled

**Actual Result:**

* User was redirected to the cart page
* Product remained in the cart
* Cart badge remained unchanged

**Status:**
Pass

**Notes:**
Cancel functionality works correctly and preserves cart state

---

### Test Case ID : TC020

### Test Title   : Verify order details on checkout overview page

### Type of Testing : Functional Testing, UI Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is added to the cart

**Description:**
Verify that the checkout overview page displays correct order details before completing the purchase.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Login using username "standard_user" and password "secret_sauce"
3. Add a product to the cart
4. Click on the cart icon
5. Click "Checkout"
6. Enter valid details (First Name, Last Name, Zip/Postal Code)
7. Click "Continue"
8. Observe the checkout overview page

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* First Name: aaa
* Last Name: bbb
* Zip/Postal Code: 12345
* Product: Any item

**Expected Result:**

* Checkout overview page should be displayed
* Selected product(s) should be listed correctly
* Product name, price, and quantity should be accurate
* Total price (including tax, if applicable) should be calculated correctly
* Payment and shipping information should be displayed

**Postcondition:**

* User is ready to complete the order

**Actual Result:**

* Checkout overview page displayed correctly
* Product details (name, price, quantity) were accurate
* Total price calculated correctly
* Payment and shipping information displayed

**Status:**
Pass

**Notes:**
Order overview displays accurate and complete information before final purchase

---
