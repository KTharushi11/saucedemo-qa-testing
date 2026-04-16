# Bug Report

---

## Defect ID

**D_SauceDemo_Checkout_001**

---

## Defect Title

**Checkout allows invalid postal code format without validation**

---

## Defect Description / Steps to Reproduce

1. Login to https://www.saucedemo.com using valid credentials
2. Add any product to the cart
3. Click on the cart icon
4. Click **"Checkout"**
5. Enter the following details:

   * First Name: aaa
   * Last Name: bbb
   * Zip/Postal Code: abc@123
6. Click **"Continue"**

---

## Expected Result

* System should validate the postal code format
* User should not be allowed to proceed
* An appropriate error message should be displayed

---

## Actual Result

* System accepts invalid postal code input
* User is allowed to proceed to the next step
* No validation error message is displayed

---

## Evidence / Attachment


---

## Severity

**Medium**

---

## Priority

**High**

---

## Module Affected

**Checkout**

---

## Environment

* Browser: Google Chrome (Latest Version)

---

## Status

**Open**

---

