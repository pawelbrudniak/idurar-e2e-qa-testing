# 🧪 TC-LOGIN-02: Verify login with invalid credentials

---

## 📌 Objective
Verify that the system prevents login when invalid credentials are provided.

---

## ⚙️ Preconditions
- Application is accessible
- User is on the login page

---

## 🧾 Test Data
- Email: invalid_user@example.com
- Password: WrongPassword123

---

## 🔢 Steps
1. Open login page
2. Enter invalid email
3. Enter invalid password
4. Click "Log In"

---

## ✅ Expected Result
- User is not logged in
- System displays an appropriate error message
- User remains on the login page

---

## ❌ Actual Result
- User is not logged in
- System displays error message:
  "No account with this email has been registered."
- User remains on the login page

---

## 📊 Status
Passed

---

## ⚡ Priority
High

---

## 🏷️ Type
Functional / Negative

---

## 🔗 Related Issue
BUG-LOGIN-002

---

## 📝 Notes
This test confirms that the application correctly blocks unauthorized login attempts using invalid credentials.