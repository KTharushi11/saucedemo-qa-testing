# Login Test Cases

---

### Test Case ID : TC001

### Test Title   : Verify login with valid credentials

### Type of Testing : Functional Testing

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

### Type of Testing : Functional Testing, Negative Testing

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

### Type of Testing : Validation Testing, Negative Testing

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

### Type of Testing : Functional Testing, Negative Testing

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

### Test Case ID : TC005

### Test Title   : Verify login with locked out user

### Type of Testing : Functional Testing, Security Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active
* Locked user account "locked_out_user" exists in the system

**Description:**
Verify that the system prevents login when a locked-out user attempts to log in with valid credentials.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter username "locked_out_user" in the Username field
3. Enter password "secret_sauce" in the Password field
4. Click on the Login button

**Test Data:**

* Username: locked_out_user
* Password: secret_sauce

**Expected Result:**

* User should not be authenticated
* User should remain on the login page
* System should display an error message indicating that the user account is locked
* No user session should be created

**Postcondition:**

* Login attempt is rejected
* User account remains locked
* User remains unauthenticated

**Actual Result:**

* System displayed error message "Epic sadface: Sorry, this user has been locked out."
* User remained on the login page

**Status:**
Pass

**Notes:**
System correctly restricts access for locked-out users and enforces account status rules

---

### Test Case ID : TC006

### Test Title   : Verify login with both username and password incorrect

### Type of Testing : Functional Testing, Negative Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active

**Description:**
Verify that the system prevents login when both username and password are incorrect.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter invalid username "wrong_user" in the Username field
3. Enter invalid password "wrong_pass" in the Password field
4. Click on the Login button

**Test Data:**

* Username: wrong_user
* Password: wrong_pass

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
System correctly handles scenario where both username and password are invalid. Error message remains consistent, improving security by not revealing specific details.

---

### Test Case ID : TC007

### Test Title   : Verify password field is masked

### Type of Testing : UI Testing, Security Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched

**Description:**
Verify that the password entered in the password field is masked (hidden) for security purposes.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter password "secret_sauce" in the Password field
3. Observe the characters displayed in the Password field

**Test Data:**

* Password: secret_sauce

**Expected Result:**

* Entered password should be displayed as masked characters (eg: dots or asterisks)
* Actual password characters should not be visible on the screen

**Postcondition:**

* Password remains hidden during input

**Actual Result:**

* Password characters were displayed as masked (dots)
* Actual password was not visible

**Status:**
Pass

**Notes:**
Password masking is functioning correctly and ensures confidentiality of user input

---

### Test Case ID : TC008

### Test Title   : Verify login with SQL injection attempt

### Type of Testing : Security Testing

---

**Preconditions:**

* User is on the login page (https://www.saucedemo.com)
* Browser is launched and internet connection is active

**Description:**
Verify that the system is secure against SQL injection attempts in the login fields.

**Test Steps:**

1. Navigate to https://www.saucedemo.com
2. Enter username "' OR '1'='1" in the Username field
3. Enter password "' OR '1'='1" in the Password field
4. Click on the Login button

**Test Data:**

* Username: ' OR '1'='1
* Password: ' OR '1'='1

**Expected Result:**

* User should not be authenticated
* User should remain on the login page
* System should reject malicious input
* Error message should be displayed indicating invalid credentials
* No user session should be created
* Application should remain stable

**Postcondition:**

* Login attempt is rejected
* Application remains secure and stable

**Actual Result:**

* System displayed error message "Epic sadface: Username and password do not match any user in this service"
* User remained on the login page

**Status:**
Pass

**Notes:**
System successfully prevents SQL injection attack and handles malicious input securely

---
