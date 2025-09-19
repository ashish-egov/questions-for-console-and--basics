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
- Facility, Employee, and Project are core entities managed in the Admin Console.  

---

## 7. What is Project Mapping with Facility, Staff (Employee), and Resource/Product Variants?
- Project mapping defines how a project is linked to facilities, employees, and resources/product variants.  

---
