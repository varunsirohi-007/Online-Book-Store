# 📚 Online Book Store (SQL Project)

## 🚀 Project Overview

Designed and developed a **relational database system using PostgreSQL** to simulate a real-world online bookstore.
The project focuses on **data organization, query optimization, and business insights generation** using SQL.

This project demonstrates strong fundamentals in **data analytics, database design, and backend data handling**.

## 🎯 Key Highlights

* Designed a **normalized relational database schema**
* Managed **inventory, customers, and transactions**
* Performed **analytical queries to extract business insights**
* Applied **joins, aggregations, and subqueries** for real-world scenarios

## 🗂️ Database Schema

### 📖 Books

Stores book inventory details

* `Book_ID` (PK)
* `Title`, `Author`, `Genre`
* `Published_Year`
* `Price`, `Stock`

### 👤 Customers

Maintains customer information

* `Customer_ID` (PK)
* `Name`, `Email`, `Phone`
* `City`, `Country`

### 🛒 Orders

Tracks customer purchases

* `Order_ID` (PK)
* `Customer_ID` (FK)
* `Book_ID` (FK)
* `Order_Date`
* `Quantity`, `Total_Amount`

## ⚙️ Core Functionalities

* 📦 Inventory tracking and stock management
* 👥 Customer data storage and retrieval
* 🛍️ Order tracking and transaction management
* 📊 Revenue and sales analysis using SQL

## 🛠️ Tech Stack

* **PostgreSQL** – Database management
* **SQL** – Data querying and manipulation

  * DDL (Data Definition Language)
  * DML (Data Manipulation Language)
  * Joins & Aggregations
  * Subqueries

## 📊 Sample Business Queries

```sql
-- Total Revenue Generated
SELECT SUM(Total_Amount) AS TotalRevenue
FROM Orders;

-- Top Selling Books
SELECT Book_ID, SUM(Quantity) AS TotalSold
FROM Orders
GROUP BY Book_ID
ORDER BY TotalSold DESC;

-- Customers with Highest Purchases
SELECT Customer_ID, SUM(Total_Amount) AS TotalSpent
FROM Orders
GROUP BY Customer_ID
ORDER BY TotalSpent DESC;
```

## 🚀 Setup Guide

```sql
CREATE DATABASE OnlineBookstore;
\c OnlineBookstore;
```

Run table creation scripts from `queries.sql`.

---

## 📁 Project Structure

```
OnlineBookstore/
│── queries.sql
│── README.md
│── Books.csv
│── Orders.csv
│── Customers.csv
```

## 📈 Skills Demonstrated

* Relational Database Design
* Data Analysis using SQL
* Problem Solving with Queries
* Data Modeling & Optimization

## 🔮 Future Improvements

* Implement **OrderDetails table** for better normalization
* Add **indexes for performance optimization**
* Create **stored procedures & triggers**
* Integrate with a **frontend application (Power BI / Web App)**

## 👨‍💻 Author

**Varun Sirohi**

