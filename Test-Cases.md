# Login Test Cases

---

### Test Case ID : TC001

### Test Title   : Verify login with valid credentials

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active

**Description:**
Verify that the user is able to successfully log in using valid credentials.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter valid username "standard_user" in the Username field
3. Enter valid password "secret_sauce" in the Password field
4. Click on the Login button

**Test Data:**

* Username: standard_user
* Password: secret_sauce

**Expected Result:**

* User should be successfully authenticated
* User should be redirected to the Inventory page
* Inventory items list should be displayed
* No error messages should be visible

**Postcondition:**

* User session is created and active
* User remains logged into the system

**Actual Result:**

* User successfully logged in
* Redirected to Inventory page with products displayed

**Status:**
Pass

**Notes:**
Login functionality is working as expected with valid credentials

---

### Test Case ID : TC002

### Test Title   : Verify login with invalid password

---

**Preconditions:**

* User is on the login page
* Valid username exists in the system

**Description:**
Verify that the system displays an appropriate error message when an incorrect password is entered.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter valid username "standard_user"
3. Enter invalid password "wrong123"
4. Click on the Login button

**Test Data:**

* Username: standard_user
* Password: wrong123

**Expected Result:**

* User should not be logged into the system
* Error message "Username and password do not match" should be displayed
* User should remain on the login page
* No session should be created

**Postcondition:**

* No user session is created
* Login attempt is rejected

**Actual Result:**

* System displayed error message "Username and password do not match"
* User remained on login page

**Status:**
Pass

**Notes:**
Error handling works correctly for invalid password scenario

---

### Test Case ID : TC003

### Test Title   : Verify login with empty fields

---

**Preconditions:**

* User is on the login page

**Description:**
Verify that the system validates mandatory fields when login form is submitted with empty inputs.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Leave Username field empty
3. Leave Password field empty
4. Click on the Login button

**Test Data:**

* Username: (empty)
* Password: (empty)

**Expected Result:**

* System should display validation error message "Username is required"
* User should not be logged in
* User should remain on login page
* No session should be created

**Postcondition:**

* Login is blocked
* User remains unauthenticated

**Actual Result:**

* System displayed error message "Username is required"
* User remained on login page

**Status:**
Pass

**Notes:**
Mandatory field validation is functioning correctly

---

### Test Case ID : TC004

### Test Title   : Verify login with invalid username

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active

**Description:**
Verify that the system prevents login when an invalid username is entered with a valid password.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter invalid username "invalid_user" in the Username field
3. Enter valid password "secret_sauce" in the Password field
4. Click on the Login button

**Test Data:**

* Username: invalid_user
* Password: secret_sauce

**Expected Result:**

* User should not be authenticated
* User should remain on the login page
* Error message should be displayed indicating invalid credentials
* No user session should be created

**Postcondition:**

* Login attempt is rejected
* User remains unauthenticated

**Actual Result:**

* System displayed error message "Epic sadface: Username and password do not match any user in this service"
* User remained on the login page

**Status:**
Pass

**Notes:**
System correctly handles invalid username scenario and prevents unauthorized access

---
