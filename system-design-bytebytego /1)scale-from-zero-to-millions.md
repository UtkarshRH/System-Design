# 🚀 System Design Day 1: Scale From Zero to Millions of Users

## 📌 What I Learned Today

Today I learned how a system grows from a **single server setup** to a system that can handle **millions of users**.

---

# 🧱 1. Single Server Architecture

### ✅ Concept:
In the beginning, everything runs on a **single server**:
- Backend (Node.js / API)
- Database (MongoDB / SQL)
- Business logic
- Cache (if any)

### 🔄 Request Flow:
1. User enters domain (e.g. api.mysite.com)
2. DNS resolves domain → IP address
3. Request goes to server
4. Server returns HTML / JSON response

### ⚠️ Problem:
- Cannot handle high traffic
- No backup (single point of failure)
- Server crash = entire system down

---

# 🏗️ 2. Two-Tier Architecture (Web + Database Separation)

### ✅ Concept:
Split system into:
- **Web Server (App Layer)**
- **Database Server (Data Layer)**

### 💡 Benefits:
- Better scalability
- Separation of concerns
- Independent scaling of backend and database

---

# 🗄️ 3. Database Types

## 🔵 SQL (Relational Database)
Examples: MySQL, PostgreSQL

### Use When:
- Structured data (tables)
- Relationships (JOIN operations)

### Example:
Banking systems, ERP systems

---

## 🟡 NoSQL (Non-Relational Database)
Examples: MongoDB, DynamoDB

### Use When:
- Unstructured or flexible data (JSON)
- High scalability required
- Fast read/write operations

### Example:
Social media apps, real-time systems

---

# ⚙️ 4. Scaling Strategies

## 🔼 Vertical Scaling (Scale Up)
- Increase CPU, RAM of a single server

### ❌ Limitations:
- Hardware limit exists
- No fault tolerance
- Expensive

---

## 🔁 Horizontal Scaling (Scale Out)
- Add multiple servers

### ✅ Advantages:
- Handles high traffic
- Fault tolerant
- Highly scalable

---

# 🚨 5. Problems in Basic Architecture

### ❌ Single Point of Failure:
If server goes down → entire app is down

### ❌ Performance Issues:
Too many users → slow response or crash

---

# 💡 6. Introduction to Load Balancer

### ✅ Concept:
Distributes incoming traffic across multiple servers

### 🔄 Flow:
User → Load Balancer → Multiple Servers

### 🎯 Benefits:
- Prevents server overload
- Improves availability
- Enables horizontal scaling

---

# 🧠 Key Takeaways

- Always **start simple** (single server)
- **Separate concerns** (web layer & data layer)
- Use **horizontal scaling** for large systems
- Avoid **single point of failure**
- Use a **load balancer** to manage traffic

---

# 🔗 Real-World Mapping (My Stack)

### 🛠️ Current Stack:
- React (Frontend)
- Node.js (Backend)
- MongoDB (Database)

### 📈 Scaling Path:
1. Single server (Node + MongoDB)
2. Separate backend & database
3. Multiple backend servers
4. Add load balancer
5. Add caching (Redis) & optimizations

---

# 🚀 Next Step

Next, I will learn:
- Load Balancer (Deep Dive)
- Caching (Redis)
- CDN
- Microservices Architecture

---
