# SQL Developer Internship - Task 1: E-commerce Schema Design

## 🎯 Objective

To learn to create a normalized database schema, define entities, and establish relationships using **Data Definition Language (DDL)** commands.

---

## 💻 Schema Overview

**Domain Chosen:** E-commerce (Retail/Sales)

**Entities (Tables) Created:**
1.  **Customers:** Stores individual customer information.
2.  **Products:** Stores item details, price, and inventory.
3.  **Orders:** Records details about a specific purchase transaction.
4.  **Order_Items:** A junction table detailing which products were included in which orders.

---

## ✅ Key Database Concepts Demonstrated

This schema design successfully implements the following core concepts:

* **Normalization (3NF):** The design is in the Third Normal Form (3NF) by isolating related data into separate tables (`Customers`, `Products`) and using a junction table (`Order_Items`) to resolve the Many-to-Many relationship between **Orders** and **Products**.
* **DDL:** Used `CREATE DATABASE` and `CREATE TABLE` commands.
* **Primary Keys (PK) & Surrogate Keys:** Used **`AUTO_INCREMENT`** for unique, system-generated Primary Keys on `Customers`, `Products`, and `Orders`.
* **Foreign Keys (FK):** Defined relationships between tables (e.g., `customer_id` in `Orders` references `Customers`).
* **Composite Key:** The `Order_Items` table uses a composite key consisting of **`(order_id, product_id)`** to uniquely identify each item line within an order.
* **Constraints:** Applied **`NOT NULL`** to required fields and a **`UNIQUE`** constraint to the `email` column in the `Customers` table.

---

## 🖼️ Entity Relationship Diagram (ERD)

The diagram below visually represents the **One-to-Many** relationships established by the Foreign Keys in the schema.

![E-commerce Schema ER Diagram](ecommerce_er_diagram.png)

---

## 📁 Repository Files

* **`ecommerce_schema.sql`**: The complete SQL script containing the DDL commands to create the tables, along with DML commands for sample data insertion.
* **`ecommerce_er_diagram.png`**: The visual Entity Relationship Diagram exported from draw.io/PlantUML.
* **`README.md`**: This summary document.
