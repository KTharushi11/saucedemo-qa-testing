# Test Summary Report

---

### 1. Purpose

This document summarizes the testing activities performed for the **SauceDemo web application**.
It includes details about test execution, defects identified, and overall system quality.

---

### 2. Application Overview

SauceDemo is a web-based e-commerce application used for testing purposes.
Users can:

* Login with valid credentials
* Add/remove products to/from cart
* Perform checkout and complete orders

Modules covered:

* Login
* Cart
* Checkout

---

### 3. Testing Scope

### a) In Scope

* Login Module
* Cart Module
* Checkout Module

---

### b) Out of Scope

* Performance Testing
* Automation Testing
* Advanced Security Testing

---

### c) Items Not Tested

* Third-party integrations (not applicable)

---

### 4. Metrics

### d) Test Cases Planned vs Executed

| Test Cases Planned | Test Cases Executed |
| ------------------ | ------------------- |
| 20                 | 20                  |

---

### e) Test Cases Pass/Fail

| Total Test Cases | Passed | Failed |
| ---------------- | ------ | ------ |
| 20               | 19     | 1      |

---

### f) Defects Identified (Status & Severity)

| Severity  | Closed | Open  |
| --------- | ------ | ----- |
| Critical  | 0      | 0     |
| Major     | 0      | 0     |
| Medium    | 0      | 1     |
| Cosmetic  | 0      | 0     |
| **Total** | **0**  | **1** |

---

### g) Defect Distribution – Module Wise

| Module    | Defects |
| --------- | ------- |
| Login     | 0       |
| Cart      | 0       |
| Checkout  | 1       |
| **Total** | **1**   |

---

### 5. Types of Testing Performed

* Functional Testing
* Negative Testing
* Validation Testing
* UI Testing
* Basic Security Testing

---

### 6. Test Environment & Tools

| Item            | Details                   |
| --------------- | ------------------------- |
| Application URL | https://www.saucedemo.com |
| Browser         | Google Chrome             |
| Testing Type    | Manual Testing            |
| Tools Used      | GitHub                    |

---

### 7. Lessons Learnt

| No | Issue Faced                                    | Solution                                |
| -- | ---------------------------------------------- | --------------------------------------- |
| 1  | Lack of strict input validation in application | Identified and reported as defect       |
| 2  | No formal requirement document                 | Used system behavior and best practices |

---

### 8. Recommendations

* Implement validation for postal code format (numeric/standard format)
* Improve input validation rules in checkout process
* Add validation feedback for incorrect formats

---

### 9. Best Practices

* Test cases organized module-wise
* Covered positive, negative, and edge cases
* Maintained clear documentation
* Included defect tracking

---

### 10. Exit Criteria

| Criteria                    | Status |
| --------------------------- | ------ |
| All test cases executed     | Yes    |
| All critical defects closed | Yes    |
| No blocking issues present  | Yes    |

---

### 11. Conclusion / Sign Off

Testing identified **1 medium severity defect** in the checkout module related to missing postal code validation.

* No critical or major defects found
* Core functionalities are working as expected
* Minor improvements required in validation

The system is **functionally stable but requires minor enhancements before production use**.

---

### 12. Definitions, Acronyms, and Abbreviations

| Term | Meaning           |
| ---- | ----------------- |
| QA   | Quality Assurance |
| TC   | Test Case         |
| UI   | User Interface    |

---
