# Login Test Cases

---

### Test Case ID : TC001  
### Test Title   : Verify login with valid credentials  

---

**Description:**  
Verify that user can login using valid username and password.

**Test Case Steps:**  
1. Open https://www.saucedemo.com  
2. Enter username  
3. Enter password  
4. Click Login button  

**Test Data:**  
Username: standard_user  
Password: secret_sauce  

**Expected Result:**  
User should be redirected to inventory page  

**Postcondition:**  
User session is active and user is logged in  

**Actual Result:**  
User successfully logged in and navigated to inventory page  

**Status:**  
Pass  

**Notes:**  
Login functionality working correctly  

---

### Test Case ID : TC002  
### Test Title   : Verify login with invalid password  

---

**Description:**  
Verify that system displays appropriate error message when user enters incorrect password.

**Test Case Steps:**  
1. Open https://www.saucedemo.com  
2. Enter username: standard_user  
3. Enter password: wrong123  
4. Click Login button  

**Test Data:**  
Username: standard_user  
Password: wrong123  

**Expected Result:**  
System should display error message "Username and password do not match" and prevent login  

**Postcondition:**  
User remains on login page and no session is created  

**Actual Result:**  
System displayed error message "Username and password do not match" and user remained on login page  

**Status:**  
Pass  

**Notes:**  
Error message is clearly visible and login is blocked successfully

---

