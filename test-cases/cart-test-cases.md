### Test Case ID : TC009

### Test Title   : Verify adding a product to cart

### Type of Testing : Functional Testing, UI Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials

**Description:**
Verify that the user can add a product to the cart successfully and UI updates accordingly.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter username "standard_user"
3. Enter password "secret_sauce"
4. Click Login button
5. Click "Add to Cart" button for any product (e.g., Sauce Labs Backpack)

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* Product: Sauce Labs Backpack

**Expected Result:**

* Product should be added to the cart
* Cart icon badge should update to show "1"
* "Add to Cart" button should change to "Remove"

**Postcondition:**

* Product is added to cart

**Actual Result:**

* Product was added successfully
* Cart badge displayed "1"
* Button changed to "Remove"

**Status:**
Pass

**Notes:**
Add to cart functionality works correctly and UI elements update as expected

---

