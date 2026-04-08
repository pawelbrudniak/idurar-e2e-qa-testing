# 🧪 TC-LOGIN-03: Verify login validation with empty fields

---

## 📌 Objective
Verify that the system prevents login when required fields are empty and displays appropriate validation messages.

---

## ⚙️ Preconditions
- Application is accessible
- User is on the login page

---

## 🧾 Test Data
- Email: (empty)
- Password: (empty)

---

## 🔢 Steps
1. Open login page
2. Leave the email field empty
3. Leave the password field empty
4. Click "Log In"

---

## ✅ Expected Result
- User is not logged in
- System displays validation messages for required fields
- Login request is not sent to the backend
- User remains on the login page

---

## ❌ Actual Result
(To be filled after execution)

Possible outcomes:
- No validation is triggered ❌
- Request is sent to the backend ❌
- Incorrect or unclear error message ❌
- Proper validation is displayed ✅

---

## 📊 Status
To be tested

---

## ⚡ Priority
High

---

## 🏷️ Type
Functional / Validation / Negative

---

## 🔗 Related Issues
- BUG-LOGIN-002 (if UI validation is incorrect)

---

## 📝 Notes
This test focuses on frontend validation only (no backend interaction expected).