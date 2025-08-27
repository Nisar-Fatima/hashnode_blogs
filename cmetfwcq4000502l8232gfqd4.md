---
title: "My Week 1 Learning Journey in DBMS"
seoTitle: "DBMS Week 1: My Learning Experience"
seoDescription: "A beginner's guide to Database Management Systems: Learn entities, relationships, architectures, and ER model examples"
datePublished: Wed Aug 27 2025 03:53:05 GMT+0000 (Coordinated Universal Time)
cuid: cmetfwcq4000502l8232gfqd4
slug: my-week-1-learning-journey-in-dbms
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1756267546076/3cd7a579-a5bc-4681-8fce-e8f530c8c212.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1756269507136/39458704-0df9-45a8-a905-53813e89c75e.png
tags: dbms, programming-fundamentals, relational-database, er-model, learninginpublic, dbms-basics

---

## Introduction

This week, I started my journey into **Database Management Systems (DBMS)**. Instead of just keeping notes to myself, I’ve decided to share my **weekly learnings** here so that others who are also studying DBMS can benefit from the same resources.

Along with learning theory, I also tried implementing concepts through **ER diagrams**, which made the ideas much clearer.

---

## What I Learned This Week

### LEC-1: Introduction to DBMS

* Difference between **Data and Information**
    
* Types of Data → *Quantitative vs Qualitative*
    
* Why we need **Databases** and what makes **DBMS better than file systems**
    
* Advantages of DBMS → *less redundancy, more security, consistency, concurrency support*
    
* This concept is explained comprehensively in the following lecture
    
* %[https://youtu.be/TYo_CUnIWP8?si=azisjX_deTUI6xPM] 
    

---

### LEC-2: DBMS Architecture

* **Three Schema Architecture** → Physical, Logical, and View levels
    
* Concept of **Schema vs Instance**
    
* **Data Models** → ER, Relational, Object-oriented
    
* **Database Languages** → DDL & DML
    
* Role of the **Database Administrator (DBA)**
    
* **DBMS Application Architectures** → 1-tier, 2-tier, and 3-tier
    
* This concept is explained comprehensively in the following lecture
    
* %[https://youtu.be/mYI2nopkQJE?si=HmEJ-xYJraudWMNS] 
    

---

### LEC-3: Entity-Relationship (ER) Model

* What **entities** and **entity sets** are
    
* Types of **Attributes** → Simple, Composite, Multi-valued, Derived
    
* **Relationships** → Strong vs Weak
    
* **Mapping Cardinalities** → One-to-One, One-to-Many, Many-to-One, Many-to-Many
    
* **Participation Constraints** → Total vs Partial
    
* This concept is explained comprehensively in the following lecture
    
* %[https://youtu.be/kMHJhhIx5k4?si=6w34KnD9DO0AV2o8] 
    

---

### LEC-4: Extended ER (EER) Features

* **Specialization** (Top-Down approach)
    
* **Generalization** (Bottom-Up approach)
    
* **Attribute Inheritance**
    
* **Aggregation** (representing relationships among relationships)
    
* This concept is explained comprehensively in the following lecture
    
* %[https://youtu.be/8_dMPX6_qiY?si=vXBHroDgKb7i-Zi4] 
    

---

## **Core Approach (Step by Step Guide + Examples)**

1. **Identify Entity Sets** (e.g., Student, Customer, Post, Employee)
    
2. **Identify Attributes** of each entity (simple, composite, multivalued, derived).
    
3. **Assign Data Types & Keys** (PK, FK, unique, nullable).
    
4. **Identify Relationships** between entities:
    
    * Strong or Weak
        
    * Degree (Unary, Binary, Ternary)
        
    * Mapping Cardinality (1:1, 1:N, M:N)
        
    * Participation Constraints (Total / Partial).
        

### **Example 1: Banking System ER Model**

A banking system is one of the most popular examples used in DBMS.

* **Entities:**
    
    * *Branch* (Branch\_ID, Name, Location, Opening\_Date)
        
    * *Employee* (Employee\_ID, Name, Role, Salary, Manager\_ID, Branch\_ID)
        
    * *Customer* (Customer\_ID, Name, DOB, Address, Contact Numbers)
        
    * *Account* (Account\_No, Balance, Date\_Opened, Status)
        
    * *Loan* (Loan\_ID, Loan\_Type, Amount, Interest\_Rate, Tenure)
        
    * *Transaction* (Transaction\_ID, Date\_Time, Amount, Type)
        
    * *Card* (Card\_No, Expiry, CVV, Card\_Type)
        
* **Special Features:**
    
    * Composite attribute: *Address* (Street, City, State).
        
    * Multivalued: Customer may have multiple phone numbers.
        
    * Weak entities: *Transaction* (depends on Account), *Card* (depends on Account).
        
    * Derived: Age (from DOB), Account\_Age (from Date\_Opened).
        
* **Relationships:**
    
    * Branch–Employee: One branch employs many employees (1:N).
        
    * Customer–Account: One customer can own multiple accounts (1:N).
        
    * Account–Transaction: An account can have multiple transactions (1:N).
        
    * Employee–Employee: Supervisor relation (Unary).
        
    * Loan–Customer: A customer can take multiple loans (1:N).
        

---

### **Example 2: Online Delivery System ER Model**

Think about Swiggy, Foodpanda, or Uber Eats.

* **Entities:**
    
    * *Customer* (Customer\_ID, Name, Contact, Address).
        
    * *Vendor/Restaurant* (Vendor\_ID, Name, Address).
        
    * *Employee/Delivery Person* (Employee\_ID, Name, Role).
        
    * *Branch* (Branch\_ID, Location).
        
    * *Order* (Order\_ID, Date, Status).
        
    * *Payment* (Payment\_ID, Mode, Amount).
        
    * *Delivery* (Delivery\_ID, Time, Status).
        
* **Special Features:**
    
    * Generalization: *Order → FoodOrder, ParcelOrder*.
        
    * Weak entity: *Order\_Item* (depends on Order).
        
    * Derived: Total\_Price (calculated from items).
        
* **Relationships:**
    
    * Customer–Order: One customer can place many orders (1:N).
        
    * Order–Payment: Each order has exactly one payment (1:1).
        
    * Vendor–Order: Vendor fulfills multiple orders (1:N).
        
    * Employee–Delivery: Delivery person delivers multiple orders (1:N).
        

---

### **Example 3: University System ER Model**

Universities are classic DBMS case studies.

* **Entities:**
    
    * *Student* (Student\_ID, Name, Roll\_No, DOB).
        
    * *Professor* (Professor\_ID, Name, Dept, Salary).
        
    * *Department* (Dept\_ID, Name, Location).
        
    * *Course* (Course\_ID, Title, Credits).
        
    * *Classroom* (Room\_No, Capacity).
        
    * *Exam* (Exam\_ID, Date, Type).
        
    * *Result* (Result\_ID, Marks, Grade).
        
* **Special Features:**
    
    * Weak entity: *Result* (depends on Student + Exam).
        
    * Unary: Professor mentors another Professor.
        
    * Multivalued: Student may have multiple contact numbers.
        
* **Relationships:**
    
    * Student–Course: Many-to-Many (M:N Enrolls).
        
    * Professor–Course: One professor teaches many courses (1:N).
        
    * Department–Professor: Department has many professors (1:N).
        
    * Exam–Student–Result: Aggregation (Result depends on both Exam and Student).
        

---

### **Example 4: Facebook ER Model**

Social networks are very rich examples.

* **Entities:**
    
    * *User* (User\_ID, Name, Email, Password, DOB).
        
    * *Post* (Post\_ID, Content, Media, Created\_At).
        
    * *Story* (Story\_ID, Content, Expiry\_At, Visibility).
        
    * *Reaction* (Reaction\_ID, Type, Emoji).
        
    * *View* (Viewer\_ID, Story\_ID, View\_Time).
        
    * *Comment* (Comment\_ID, Content, Created\_At).
        
    * *Like* (Like\_ID, Reaction\_Type).
        
    * *Friendship* (Friendship\_ID, Request\_Status).
        
    * *Group, Group\_Membership* (Admin, Role).
        
    * *Page, Page\_Follow* (Page\_Name, Category).
        
    * *Message* (Message\_ID, Sender, Receiver, Content).
        
* **Special Features:**
    
    * Weak entities: *Comment, Like, View*.
        
    * Unary: *Friendship* (User–User).
        
    * Associative: *Group\_Membership, Page\_Follow*.
        
    * Aggregation: *Story–Reaction–View*.
        
* **Relationships:**
    
    * User–Post (1:N).
        
    * Post–Comment (1:N).
        
    * User–User (Friendship M:N).
        
    * Story–View (M:N).
        
    * Story–Reaction (M:N).
        

---

### **Example 5: Instagram ER Model**

* **Entities:**
    
    * *User* (User\_ID, Username, Email, DOB, Bio).
        
    * *Post* (Post\_ID, Content, Media, Hashtags).
        
    * *Comment* (Comment\_ID, Content, User\_ID).
        
    * *Like* (Like\_ID, Type).
        
    * *Story* (Story\_ID, Expiry\_At).
        
    * *Reel* (Reel\_ID, Media, Audio).
        
    * *Hashtag* (Tag\_ID, Tag\_Name).
        
    * *Message* (Message\_ID, Sender, Receiver, Content).
        
    * *Follower* (Follower\_ID, Following\_ID).
        
* **Special Features:**
    
    * Weak: *Comment, Like, Reel\_Comment, Reel\_Like*.
        
    * Associative: *Follower, Post\_Hashtag*.
        
    * Unary: *Follower* (User follows User), *Messages* (User ↔ User).
        
    * Derived: *Age (DOB)*.
        
* **Relationships:**
    
    * User–Post: One user can create multiple posts (1:N).
        
    * Post–Hashtag: Posts can have multiple hashtags (M:N).
        
    * User–Follower: One user can follow multiple users (Unary M:N).
        
    * User–Story: One user can post multiple stories (1:N).
        
    * Reel–Like: Reels can have multiple likes (1:N).
        

---

# ER Diagram → Relational Model Conversion Rules:

👉 Converting **ER design** into **Relational design** is a crucial step in building a database. Let’s break down how each ER concept maps into a relational schema.

## 1\. Strong Entity

* Each **strong entity** becomes an **individual table**.
    
* Attributes → Columns in the table.
    
* Primary Key (PK) → Entity’s PK is directly the relation’s PK.
    
* Foreign Keys (FKs) → Added to establish relationships with other entities.
    

Example:  
`Customer(Customer_ID [PK], Name, Email, Phone)`

---

## 2\. Weak Entity

* A **weak entity** cannot exist without its strong entity.
    
* Becomes a separate table.
    
* PK of strong entity is added as FK.
    
* Composite PK = {Strong Entity PK (FK) + Discriminator Key}.
    

Example:  
`Order_Item(Order_ID [FK], Item_No, Quantity, PRIMARY KEY(Order_ID, Item_No))`

---

## 3\. Single-Valued Attributes

* Directly represented as **columns** in the table.
    
* No extra table is needed.
    

Example: `Salary`, `Date_Of_Joining`

---

## 4\. Composite Attributes

* Break into **atomic attributes** in the main table.
    
* Do not keep the composite attribute as a column.
    

Example:  
Instead of `Address`, store → `Street, City, State, Zip`.

---

## 5\. Multivalued Attributes

* Stored in a **separate table**.
    
* Table includes entity’s PK as FK + multivalued attribute.
    
* PK of new table = {Entity\_PK + Multivalued Attribute}.
    

Example:

* `Employee(Emp_ID [PK], Name)`
    
* `Employee_Phone(Emp_ID [FK], Phone_No, PRIMARY KEY(Emp_ID, Phone_No))`
    

---

## 6\. Derived Attributes

* Not stored in relations.
    
* Calculated when needed.
    

Example: `Age` derived from `DOB`.

---

## 7\. Generalization / Specialization

### Method 1 (Default)

* Create a **table for the supertype**.
    
* Create separate **tables for each subtype**, including subtype attributes + supertype PK (as FK).
    

Example (Bank Account):

* `Account(Account_No [PK], Balance)`
    
* `Savings_Account(Account_No [FK, PK], Interest_Rate)`
    
* `Current_Account(Account_No [FK, PK], Overdraft_Limit)`
    

### Method 2 (Disjoint + Complete Generalization)

* Skip the supertype table.
    
* Create tables for subtypes including both supertype and subtype attributes.
    

Example:

* `Savings_Account(Account_No [PK], Balance, Interest_Rate)`
    
* `Current_Account(Account_No [PK], Balance, Overdraft_Limit)`
    

**Drawback:** If overlapping/generalization is not complete → redundancy & missing data risk.

---

## 8\. Aggregation

* Represented as a **relationship table**.
    
* Includes PKs of all participating entities + descriptive attributes.
    

Example:  
Customer places Order → generates Payment.  
`Order_Payment(Customer_ID [FK], Order_ID [FK], Payment_ID [FK], Payment_Mode, Amount)`

## Resources I Used

Along with standard references, I especially followed **DBMS YouTube Series(** *CodeHelp-by babbar DBMS Series)*, which explained the concepts in a very simple and student-friendly way.his playlist explains DBMS concepts in a **simple and student-friendly way**.

👉 What’s even better: **each video has detailed notes provided in the description/under the video**, so you don’t need to write everything yourself. You can directly learn, revise, and practice using them

Other helpful resources:

* 📘 *Database System Concepts* by Silberschatz, Korth, Sudarshan
    
* 🌐 GeeksforGeeks DBMS Notes
    
* 🌐 TutorialsPoint DBMS Tutorial
    

---

## Conclusion

That’s a wrap for my **Week 1 of DBMS learning**.  
The biggest takeaway for me was that **databases are not just about storage, but about meaningful organization of data into useful information**.

From next week, I’ll continue hands-on practice on **SQL Workbench**, where I’ll be writing and testing queries. I’ll also put together a list of **important SQL queries** that can help beginners get started easily.

Stay tuned for my updates — it’s going to be fun and practical!