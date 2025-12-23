# 🚗 Vehicle Rental System – Database Design & SQL Queries

## 📌 Project Overview
This project demonstrates the design and implementation of a **Vehicle Rental System** database.  
The assignment focuses on **ERD design**, **relational database concepts**, and **SQL querying techniques** such as JOIN, EXISTS, WHERE, GROUP BY, and HAVING.

The system manages:
- Users (Admin and Customer)
- Vehicles
- Bookings

---

## 🧩 Database Design
The database consists of three core tables:

### 1. Users
Stores user information such as name, email, phone number, and role (Admin or Customer).  
Each user can make multiple bookings.

### 2. Vehicles
Stores vehicle details including name, type (car/bike/truck), model, registration number, rental price, and availability status.

### 3. Bookings
Stores rental booking information including booking dates, booking status, total cost, and references to users and vehicles.

### 🔗 Relationships
- One User → Many Bookings
- One Vehicle → Many Bookings
- Each booking is associated with exactly one user and one vehicle

---

## 📊 SQL Queries Explanation

All SQL queries are provided in the **queries.sql** file.

### Query 1: INNER JOIN
Retrieves booking details along with customer name and vehicle name by joining Users, Vehicles, and Bookings tables.

### Query 2: NOT EXISTS
Finds vehicles that have never been booked using a NOT EXISTS subquery.

### Query 3: WHERE
Retrieves all available vehicles of a specific type (e.g., cars).

### Query 4: GROUP BY & HAVING
Counts total bookings per vehicle and displays only those vehicles that have more than two bookings.

---

## 🛠 Tools & Technologies Used
- MySQL (SQL Queries)
- Lucidchart (ERD Design)
- GitHub (Version Control & Submission)

---

## 📎 Submission Links
- **GitHub Repository:** _[Add your GitHub repo link here]_
- **ERD Link:** _[Add your Lucidchart public ERD link here]_
- **Viva Video Link:** _[Add your YouTube or Google Drive link here]_

---

## 🎯 Learning Outcomes
- Understanding relational database design
- Applying primary key and foreign key constraints
- Writing optimized SQL queries
- Explaining database concepts clearly in viva
