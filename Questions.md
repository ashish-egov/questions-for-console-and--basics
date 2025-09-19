# Kafka and Admin Console Basics (Training Notes)

## 1. How does Kafka decide which partition will get a message?
- If a **key** is provided → Kafka always sends messages with the same key to the same partition (ordering maintained).  
- If **no key** is provided → Kafka distributes messages in a **round-robin** manner (for load balancing).  

---

## 2. What is a Consumer Group?
- A **Consumer Group** is a set of consumers reading from the same topic.  
- Kafka ensures that each partition’s data goes to **only one consumer in the group**.  
- This avoids duplicate processing and allows scaling.  

---

## 3. What is Rebalancing in Kafka?
- When a **new consumer joins**, or an **existing one leaves/crashes**, Kafka reassigns partitions among available consumers.  
- This process is called **Rebalancing**.  
- During rebalancing, consumers may temporarily **stop reading messages**.  

---

## 4. What are Offsets in Kafka?
- **Offset** = the position of a message in a partition.  
- Consumers use offsets to track which messages have been read.  
- Offsets can be:
  - **Auto-committed** (Kafka commits automatically).  
  - **Manually committed** (application decides when to commit).  

---

## 5. How does Kafka handle Failures (High Availability)?
- Each partition has a **Leader** and multiple **Followers (replicas)**.  
- Producers and consumers always talk to the **Leader**.  
- If the leader fails → one of the followers is automatically promoted to **new leader**.  

---

## 6. What are Facility, Employee, and Project in the Admin Console?
- **Facility** → A physical or virtual location where work takes place  
  (e.g., hospital, school, warehouse, training center).  
- **Employee (Staff)** → A person working in or assigned to a facility  
  (e.g., teacher, nurse, operator).  
- **Project** → An initiative or program executed at a facility  
  (e.g., vaccination drive, training program, product distribution).  

**Summary:**  
Admin Console manages **Facilities (where)**, **Employees (who)**, and **Projects (what work/initiative)**.  

---

## 7. What is Project Mapping with Facility, Staff (Employee), and Resource/Product Variants?
- **Project → Facility mapping**: Defines **where** a project will run.  
- **Project → Staff (Employee) mapping**: Assigns **who** will work on the project.  
- **Project → Resource/Product Variants mapping**: Links **what resources/products** are required  
  (e.g., medicine types, training materials, product SKUs).  

**Summary:**  
Project mapping connects **location, people, and resources** for proper execution and tracking.  

---
