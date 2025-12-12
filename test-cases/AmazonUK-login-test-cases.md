# Amazon.co.uk Login – Test Cases

## Scope
Testing login functionality for Amazon UK web application.

## Assumptions
- User has a registered Amazon UK account
- Internet connection is available
- Two-step verification (SMS) is enabled for the account
- Supported browsers: Chrome, Firefox

---

### TC-01: Login with valid credentials
**Preconditions:** User is registered and two-step verification is enabled. User is not logged in
**Steps:**
1. Open sign-in page
2. Enter valid email
3. Click "Continue"
4. Enter valid password
5. Click "Sign in"
6. Enter verification code received via SMS

**Expected Result:**  
User is successfully authenticated, verification code is accepted, and user is redirected to the Amazon UK main page.

---

### TC-02: Login with invalid password
**Preconditions:** User is registered and two-step verification is enabled. User is not logged in
**Steps:**
1. Open sign-in page
2. Enter valid email
3. Click "Continue"
4. Enter invalid password
5. Click "Sign in"

**Expected Result:**  
Error message indicating incorrect password is displayed. User remains on password entry step.

---

### TC-03: Login with empty fields
**Preconditions:** User is not logged in
**Steps:**
1. Open sign-in page
2. Leave email empty
3. Click "Continue"

**Expected Result:**  
Validation message is displayed.

---

### TC-04: Login with invalid email format
**Preconditions:** User is not logged in
**Steps:**
1. Open sign-in page
2. Enter invalid email format
3. Click "Continue"

**Expected Result:**  
Validation message is displayed.

---

### TC-05: Login with incorrect SMS verification code
**Preconditions:** User is registered and two-step verification is enabled  

**Steps:**
1. Open sign-in page
2. Enter valid email
3. Click "Continue"
4. Enter valid password
5. Click "Sign in"
6. Enter incorrect verification code

**Expected Result:**  
Error message is displayed indicating invalid verification code. User is not logged in and remains on verification step.
