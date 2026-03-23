# 🧩 HLD vs LLD Example (Simple)

---

## 🎯 Example: Login System

---

# 🏗️ High-Level Design (HLD)

## 💡 What we think:

Big picture of the system

## 📦 Components:

* User (Frontend)
* Server (Backend API)
* Database

## 📊 Diagram

```
   User
     |
     v
  Frontend
     |
     v
   Backend
     |
     v
  Database
```

---

# 🧱 Low-Level Design (LLD)

## 💡 What we think:

How we write code inside backend

## 📦 Components:

* User class
* Login API
* Password check logic

## 🧑‍💻 Example Code

```js
class User {
  constructor(email, password) {
    this.email = email;
    this.password = password;
  }

  login(inputPassword) {
    return this.password === inputPassword;
  }
}
```

---

# ⚡ Simple Understanding

* HLD → “System ka flow kya hai?”
* LLD → “Code ka structure kya hai?”

---

# 🚀 Summary

* HLD = Big picture
* LLD = Code level
* Start simple → go deep later
