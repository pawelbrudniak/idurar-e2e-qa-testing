# 🧪 TC-LOGIN-01: Verify login with valid credentials

---

## 📌 Objective
Verify that the user can successfully log in with valid credentials.

---

## ⚙️ Preconditions
- Application is accessible
- User is on the login page
- ⚠️ No users currently exist in the database (known issue)

---

## 🧾 Test Data
- Email: admin@admin.com
- Password: admin123

---

## 🔢 Steps
1. Open login page
2. Enter valid email
3. Enter valid password
4. Click "Login"

---

## ✅ Expected Result
User is successfully logged in and redirected to the dashboard.

---

## ❌ Actual Result
Login fails with error:
"No account with this email has been registered."

---

## 📊 Status
Failed

---

## ⚡ Priority
High

---

## 🏷️ Type
Functional

---

## 🔗 Related Issues
- BUG-LOGIN-002
- BUG-SETUP-001

---

## 📝 Notes
Failure is caused by missing user data in the database due to a broken setup script.