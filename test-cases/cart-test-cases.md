# Cart Test Cases

---

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
5. Click "Add to Cart" button for any product (eg: Sauce Labs Backpack)

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

### Test Case ID : TC010

### Test Title   : Verify removing a product from cart

### Type of Testing : Functional Testing, UI Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials
* At least one product is already added to the cart

**Description:**
Verify that the user can remove a product from the cart and UI updates accordingly.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter username "standard_user"
3. Enter password "secret_sauce"
4. Click Login button
5. Click "Add to Cart" for any product
6. Click "Remove" button for the added product

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* Product: Sauce Labs Backpack

**Expected Result:**

* Product should be removed from the cart
* Cart icon badge should update (eg: from "1" to empty)
* "Remove" button should change back to "Add to Cart"

**Postcondition:**

* Cart is updated and product is removed

**Actual Result:**

* Product was removed successfully
* Cart badge updated (removed)
* Button changed back to "Add to Cart"

**Status:**
Pass

**Notes:**
Remove from cart functionality works correctly and UI updates as expected

---

### Test Case ID : TC011

### Test Title   : Verify cart badge updates correctly

### Type of Testing : Functional Testing, UI Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* User is logged in with valid credentials

**Description:**
Verify that the cart badge displays the correct number of items when products are added or removed.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter username "standard_user"
3. Enter password "secret_sauce"
4. Click Login button
5. Click "Add to Cart" for two different products
6. Observe the cart badge count
7. Click "Remove" for one product
8. Observe the cart badge count again

**Test Data:**

* Username: standard_user
* Password: secret_sauce
* Products: Any two items

**Expected Result:**

* Cart badge should display "2" after adding two products
* Cart badge should update to "1" after removing one product
* Badge count should always reflect the exact number of items in the cart

**Postcondition:**

* Cart contains correct number of items

**Actual Result:**

* Cart badge displayed "2" after adding two products
* Cart badge updated to "1" after removing one product

**Status:**
Pass

**Notes:**
Cart badge updates dynamically and accurately reflects cart contents

---
