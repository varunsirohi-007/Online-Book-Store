# 📚 Online Book Store (SQL Project)

## 📌 Overview

This project is a **PostgreSQL-based Online Book Store Management System** designed to handle book inventory, customer records, and order transactions. It showcases practical usage of SQL for data management and analysis.

---

## 🗂️ Database Schema

The database consists of three main tables:

### 📖 Books

* `Book_ID` (Primary Key)
* `Title`
* `Author`
* `Genre`
* `Published_Year`
* `Price`
* `Stock`

### 👤 Customers

* `Customer_ID` (Primary Key)
* `Name`
* `Email`
* `Phone`
* `City`
* `Country`

### 🛒 Orders

* `Order_ID` (Primary Key)
* `Customer_ID` (Foreign Key)
* `Book_ID` (Foreign Key)
* `Order_Date`
* `Quantity`
* `Total_Amount`

---

## ⚙️ Features

* Manage book inventory and stock levels
* Store and retrieve customer details
* Track book orders and purchases
* Perform data analysis using SQL queries

---

## 🛠️ Technologies Used

* PostgreSQL
* SQL (DDL, DML, Joins, Aggregations, Subqueries)

---

## 🚀 Setup Instructions

### 1️⃣ Create Database

```sql
CREATE DATABASE OnlineBookstore;
```

### 2️⃣ Connect to Database

```sql
\c OnlineBookstore;
```

### 3️⃣ Create Tables

```sql
-- Books Table
CREATE TABLE Books (
    Book_ID SERIAL PRIMARY KEY,
    Title VARCHAR(100),
    Author VARCHAR(100),
    Genre VARCHAR(50),
    Published_Year INT,
    Price NUMERIC(10, 2),
    Stock INT
);

-- Customers Table
CREATE TABLE Customers (
    Customer_ID SERIAL PRIMARY KEY,
    Name VARCHAR(100),
    Email VARCHAR(100),
    Phone VARCHAR(15),
    City VARCHAR(50),
    Country VARCHAR(150)
);

-- Orders Table
CREATE TABLE Orders (
    Order_ID SERIAL PRIMARY KEY,
    Customer_ID INT REFERENCES Customers(Customer_ID),
    Book_ID INT REFERENCES Books(Book_ID),
    Order_Date DATE,
    Quantity INT,
    Total_Amount NUMERIC(10, 2)
);
```

---

## 🔍 Example Queries

```sql
-- Retrieve Fiction books
SELECT * FROM Books
WHERE Genre = 'Fiction';

-- Customers from Canada
SELECT * FROM Customers
WHERE Country = 'Canada';

-- Orders in November 2023
SELECT * FROM Orders
WHERE Order_Date BETWEEN '2023-11-01' AND '2023-11-30';

-- Total revenue
SELECT SUM(Total_Amount) AS TotalRevenue
FROM Orders;
```

---

## 📁 Project Structure

```
OnlineBookstore/
│── schema.sql
│── queries.sql
│── README.md
```

---

## 🎯 Learning Outcomes

* Designing relational databases
* Writing efficient SQL queries
* Using joins and aggregations
* Solving real-world data problems

---

## 🔮 Future Enhancements

* Add OrderDetails table (for normalization)
* Build frontend interface
* Add stored procedures and triggers
* Optimize queries with indexing

---

## 👨‍💻 Author

Varun Sirohi
GitHub: https://github.com/your-username

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!

