# 🏦 ATM System - Sequence Diagram (System Design)

## 🚀 Positive Thought

> "Great engineers don’t just write code — they design systems that scale."

---

# 📌 Problem Statement

Design the **ATM Withdrawal Flow** using a Sequence Diagram.

---

# 🧩 Actors & Components

* **User** → Initiates withdrawal
* **ATM** → Interface system
* **Transaction** → Handles business logic
* **Account** → Validates balance
* **Cash Dispenser** → Dispenses money

---

# 🔄 Sequence Flow (Step-by-Step)

1. User requests withdrawal
2. ATM forwards request to Transaction
3. Transaction checks balance via Account
4. Account validates and returns response
5. If valid → Transaction proceeds
6. ATM triggers Cash Dispenser
7. Cash is dispensed
8. Response returned back to User

---

# 📊 Sequence Diagram (Text Representation)

```
User        ATM        Transaction        Account        CashDispenser
 |           |              |                |                |
 |--withdraw(amount, accNo)->|              |                |
 |           |--withdraw()-->|              |                |
 |           |              |--checkBal()-->|                |
 |           |              |<--true--------|                |
 |           |<--success----|                |                |
 |           |--------------------------------------------->|
 |           |         withdrawCash(amount)                |
 |           |<---------------------------------------------|
 |<--return amount------------------------------------------|
```

---

# ⚙️ Message Types Used

## ✅ Synchronous Messages

* `withdraw()`
* `checkBalance()`

➡️ Waits for response before proceeding

---

## ⚡ Asynchronous Messages

* `withdrawCash()`

➡️ No strict wait (real-world may vary)

---

# 🧠 Key Concepts Applied

### ✔ Lifeline

Each vertical line = object lifecycle
(User, ATM, Transaction, Account, CashDispenser)

---

### ✔ Activation Bar

Shows when object is active (processing)

---

### ✔ Return Message

```
<------ return true / amount
```

---

# 🔀 Conditional Flow (ALT Example)

```
[if balance >= amount]
   proceed withdrawal
[else]
   show "Insufficient Balance"
```

---

# 🔁 Loop Example

```
[while user performs transactions]
   repeat process
```

---

# ❗ Edge Cases

* Invalid account number
* Insufficient balance
* ATM out of cash
* Network failure

---

# 🏗️ Design Insight

* ATM acts as **controller**
* Transaction handles **business logic**
* Account is **data layer**
* Cash Dispenser is **external system**

---

# ✅ Summary

* Sequence Diagram shows **real-time interaction**
* Helps in:

  * System clarity
  * Interview explanation
  * Debugging flow

---

# 🔥 Final Takeaway

> "If you can draw it clearly, you can build it confidently."

---
