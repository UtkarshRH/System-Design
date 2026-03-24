# 📘 Day 2: UML Diagrams (System Design Basics)

## 🚀 Positive Thought

> "Every complex system becomes simple when you visualize it."

---

# 📌 What is UML?

**UML (Unified Modeling Language)** is used to visually represent system design, structure, and interactions.

---

# 🧩 Types Covered Today

* Class Diagram
* Sequence Diagram

---

# 🏗️ Class Diagram

## 🔑 Access Modifiers

| Modifier  | Symbol | Access Level          |
| --------- | ------ | --------------------- |
| Public    | `+`    | Everywhere            |
| Private   | `-`    | Within class only     |
| Protected | `#`    | Class + Child classes |

---

## 🔗 Relationships in Class Diagram

### 1. Association (Simple Relationship)

* Basic connection between classes

```
User -------- Order
```

---

### 2. Aggregation (Weak "has-a")

* Container relationship (objects can exist independently)

```
Room ◇------ Furniture
```

Example:

* Room has Sofa, Bed, Chair

---

### 3. Composition (Strong "has-a")

* Strong dependency (child cannot exist without parent)

```
House ◆------ Room
```

---

## 🔺 Arrow Representations

| Type        | Symbol |
| ----------- | ------ |
| Association | ─────  |
| Inheritance | ─────▷ |
| Aggregation | ◇────  |
| Composition | ◆────  |

---

## 🚗 Example: Car System

```
              +----------------+
              |      Car       |
              +----------------+
              | +start()       |
              +----------------+
                     ▲
        ---------------------------
        |                         |
+----------------+      +-------------------+
|  ManualCar     |      |  AutomaticCar     |
+----------------+      +-------------------+
| +changeGear()  |      | +changeBattery()  |
+----------------+      +-------------------+
```

---

# 🔄 Sequence Diagram

Used to show **interaction between objects over time**

---

## 🧱 Components

### 1. Lifeline

* Represents object existence

```
User        ATM
 |           |
```

---

### 2. Activation Bar

* Shows when object is active

```
 |  ███
```

---

### 3. Messages

#### ➤ Synchronous (Wait for response)

```
User -> ATM : insertCard()
```

#### ➤ Asynchronous (No wait)

```
User --> ATM : requestBalance()
```

---

## 📩 Types of Messages

* Create Message → Object creation
* Destroy Message → Object deletion
* Lost Message → Unknown receiver
* Found Message → Unknown sender

---

## 🏦 Example: ATM System

```
User        ATM        Bank
 |           |          |
 |--insertCard()------->|
 |           |--verify()------>|
 |           |<--response------|
 |<--showMenu()---------------|
```

---

## 🔀 Control Flow

### ALT (If-Else)

```
[if balance > 0]
   withdraw()
[else]
   show error
```

### OPT (Optional)

```
[if user wants receipt]
   printReceipt()
```

### LOOP

```
[while transactions]
   processTransaction()
```

---

# 🧠 How to Draw Sequence Diagram

1. Identify Use Case (e.g., ATM withdrawal)
2. Identify Objects (User, ATM, Bank)
3. Draw Lifelines
4. Add Messages
5. Add Conditions (ALT / LOOP / OPT)

---

# ✅ Summary

* Class Diagram → Structure of system
* Sequence Diagram → Behavior / flow of system
* Relationships → Association, Aggregation, Composition
* Messages → Sync & Async

---

# 🔥 Key Learning

Understanding UML helps in:

* Better system design
* Clear communication in interviews
* Writing scalable architecture

---
