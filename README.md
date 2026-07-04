# Project 3: The Data Warehouse

## Scenario
An e-commerce company needed a secure, scalable cloud database to replace 
Excel-based customer record management.

## Mission
Set up a managed MySQL database on AWS RDS, secured in a private subnet 
with no public access, reachable only through an SSH tunnel via an EC2 
bastion host.

## Steps Completed
1. Provisioned a MySQL RDS instance (`warehouse-db`) with public access disabled
2. Launched an EC2 bastion host in the same VPC to act as a secure gateway
3. Configured security groups so RDS only accepts traffic from the bastion's 
   security group (not open to the internet)
4. Connected via MySQL Workbench using an SSH tunnel through the bastion
5. Created an `Interns` table with `PRIMARY KEY`, `UNIQUE`, and `NOT NULL` constraints
6. Inserted dummy records and verified persistence with a `SELECT` query

## Screenshots

### 1. RDS Database Available
https://github.com/user-attachments/assets/638be154-935e-4052-b05d-fed4a5377d05

### 2. Security Group Locked to Bastion
https://github.com/user-attachments/assets/281c3dc6-f2de-4958-9f01-c86f72d978ae

### 3. Successful SSH Tunnel Connection
https://github.com/user-attachments/assets/031d1c5f-39df-4c93-b231-12f02ba5da83

### 4. Table Creation and Data Insertion
https://github.com/user-attachments/assets/c6c63270-a17b-4219-9459-2c8becf8aeea

### 5. Verified Data via SELECT Query
https://github.com/user-attachments/assets/cfc92e42-bd15-4010-b42f-56f82adee452

## Tools Used
- AWS RDS (MySQL)
- AWS EC2 (Bastion Host)
- AWS Security Groups (VPC)
- MySQL Workbench (SSH Tunnel)

## Key Learning
A public-facing database is a compromised database. This project demonstrates 
proper network isolation using private subnets and security-group-based 
access control instead of relying on IP whitelisting alone.

