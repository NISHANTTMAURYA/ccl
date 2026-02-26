# 📘 Cloud Computing Lab 5 — Amazon RDS Deployment & EC2 Connectivity

## 🔹 Experiment Objective
The objective of this experiment is to deploy a managed MySQL database using Amazon RDS, securely connect it with an EC2 instance, and demonstrate database operations (CRUD). This experiment highlights real-world cloud architecture where application servers interact with managed database services instead of local storage.

---

## 🏗️ Architecture Overview
The architecture consists of:
- EC2 instance acting as the application layer
- Amazon RDS MySQL instance acting as the database layer
- Security groups enforcing controlled communication
- Private VPC connectivity between EC2 and RDS

**EC2 Public URL:**  
<ADD_EC2_PUBLIC_URL_HERE>

---

## ⚙️ AWS Services Used
- Amazon EC2
- Amazon RDS (MySQL)
- VPC (default)
- Security Groups

---

## 🚀 Step-by-Step Implementation

### Step 1 — Create Amazon RDS Database
1. Navigate to AWS Console → RDS → Databases → Create database
2. Select MySQL engine
3. Choose Free tier
4. Configure DB identifier: lab5-mysql
5. Configure credentials and launch database

RDS Endpoint: <ADD_RDS_ENDPOINT_HERE>

---

### Step 2 — Configure Security Groups
Allow inbound MySQL rule (3306) from EC2 security group.

---

### Step 3 — Connect EC2 to RDS
Install mysql client and connect using endpoint.

---

### Step 4 — Create Database and Table
CREATE DATABASE lab5db;
USE lab5db;
CREATE TABLE students(id INT PRIMARY KEY AUTO_INCREMENT, name VARCHAR(50), age INT);

---

### Step 5 — CRUD Operations
INSERT INTO students(name,age) VALUES('Nishant',20);
SELECT * FROM students;
UPDATE students SET age=21 WHERE name='Nishant';
DELETE FROM students WHERE name='Nishant';

---

## 🔐 Security Considerations
- RDS inside VPC
- Restricted via security groups
- Only EC2 allowed to connect

---

## 📊 Results
- RDS deployed
- Secure connectivity established
- CRUD verified

---

## 🔗 Submission Links
EC2 URL: <ADD_EC2_PUBLIC_URL_HERE>
GitHub Repo: <ADD_GITHUB_REPO_LINK_HERE>

---

## 📝 Author
Name: <ADD_NAME>
Roll No: <ADD_ROLL_NO>
