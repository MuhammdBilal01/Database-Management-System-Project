# Inventory Management System — SQL Server Database

A relational **Inventory Management System (IMS)** database designed and implemented to manage products, inventory, suppliers, customers, stock transactions, returns, and purchase orders.

The project focuses on **relational database design, normalization, SQL querying, database views, stored procedures, and transaction management** using Microsoft SQL Server.

---

## Project Overview

The Inventory Management System provides a structured relational database for managing inventory-related operations.

The database consists of seven core entities:

* Products
* Categories
* Suppliers
* Stock Transactions
* Returns
* Customers
* Purchase Orders

The database was designed with **Boyce-Codd Normal Form (BCNF)** as the target normalization level to reduce redundancy and improve data integrity.

The implementation demonstrates practical SQL concepts including aggregate queries, multi-table joins, subqueries, nested queries, views, stored procedures, transactions, and rollback handling.

---

## Objectives

* Efficiently track inventory levels, sales, purchases, and returns
* Maintain supplier information and purchase orders
* Manage customer information
* Maintain accurate and consistent data
* Reduce redundancy through database normalization
* Establish proper relationships between database entities
* Support inventory-related analysis through SQL queries
* Provide a structured and scalable relational database design

---

## Database Entities

| Entity             | Description                                                                    |
| ------------------ | ------------------------------------------------------------------------------ |
| Products           | Stores product information, category, SKU, price, stock level, and description |
| Categories         | Stores product categories                                                      |
| Suppliers          | Stores supplier and contact information                                        |
| Stock Transactions | Records inventory movements such as sales, purchases, and adjustments          |
| Returns            | Records returned products and return information                               |
| Customers          | Stores customer information                                                    |
| Purchase Orders    | Stores purchase-order information associated with suppliers                    |

---

## Database Relationships

The database contains relationships between the major entities:

* Products → Categories
* Products → Stock Transactions
* Suppliers → Purchase Orders
* Customers → Returns
* Stock Transactions → Returns

The project includes one-to-many and one-to-one relationships as defined in the database design.

---

## Database Design

The database was designed using relational database principles with **BCNF (Boyce-Codd Normal Form)** as the target normalization level.

The normalization process addresses:

* Atomic attributes
* Repeating groups
* Partial dependencies
* Transitive dependencies
* Candidate-key determinants
* Primary and foreign key relationships

### Products Entity

The Products entity contains:

* Product_ID — Primary Key
* Product_Name
* Category_ID — Foreign Key
* SKU
* Price
* Stock_Level
* Description

---

## SQL Implementation

The project demonstrates several SQL techniques for retrieving, analyzing, and manipulating database information.

### Aggregate Queries

The project includes queries for:

* Total Sales
* Average Price
* Total Stock
* Total Returns
* Maximum Quantity Sold
* Total Amount for Purchase Orders
* Number of Products Sold by Category

### JOIN Queries

The project demonstrates:

* INNER JOIN
* LEFT JOIN
* RIGHT JOIN
* FULL JOIN

These queries are used to retrieve related information from multiple tables.

### Subqueries and Nested Queries

The project includes examples for:

* Finding total sales for a product
* Finding average price for a category
* Finding total stock for a product
* Finding products with a price greater than the average price
* Finding products in a specific category

---

## Database Views

The project includes database views for:

### Stock Levels with Product Details

Provides product information together with stock-level information.

### Product Returns Summary

Provides summarized information related to product returns.

---

## Stored Procedures

The database includes stored procedures for important operations.

### Add Stock to a Product

A stored procedure used to update the stock level of a product.

The implementation demonstrates:

* Stored procedures
* Data modification
* Transaction management
* Rollback handling

### Update Product Price

A stored procedure used to update the price of a product while demonstrating transaction management and rollback handling.

---

## Transaction Management

Transaction management is demonstrated through the stored procedures.

Transactions are used during critical database operations to maintain atomicity and provide rollback capability when an operation needs to be reverted.

---

## Technologies Used

* Microsoft SQL Server
* SQL / T-SQL
* SQL Server Management Studio (SSMS)

---

## Database Concepts Demonstrated

* Relational Database Design
* Entity Relationship Modeling
* Database Normalization
* BCNF
* Primary Keys
* Foreign Keys
* Referential Integrity
* One-to-Many Relationships
* One-to-One Relationships
* Aggregate Functions
* SQL JOINs
* Subqueries
* Nested Queries
* Database Views
* Stored Procedures
* Transactions
* Rollback
* Database Backup and Restore

---

## Repository Contents

The repository contains:

* SQL Server database backup
* Project documentation
* SQL implementation files
* Database design documentation
* Database-related resources

---

## Database Backup

The project includes an SQL Server database backup file.

The backup can be restored using Microsoft SQL Server Management Studio to inspect the database structure, tables, data, views, and stored procedures.

### Requirements

* Microsoft SQL Server
* SQL Server Management Studio (SSMS)

### Restore Process

1. Open SQL Server Management Studio.
2. Connect to a SQL Server instance.
3. Right-click Databases.
4. Select Restore Database.
5. Select the database backup file.
6. Select the target database.
7. Review the restore settings.
8. Execute the restore.
9. Open the restored database and inspect its objects.

---

## Project Documentation

The project report contains:

* Introduction and objectives
* Database entities and attributes
* Database normalization and BCNF
* Relationships between tables
* ERD
* SQL query examples
* Aggregate queries
* JOIN queries
* Subqueries
* Nested queries
* Database views
* Stored procedures
* Transaction and rollback examples
* Database screenshots
* Backup information

---

## Project Scope

This project focuses on the **database layer** of an Inventory Management System.

The primary objective is to demonstrate practical knowledge of relational database design and SQL implementation for inventory-related operations.

The project does not include a separate front-end application.
