# 🍴 Zomato Database and Schema Project

## 📖 Overview

This project presents a relational **database schema** for a Zomato-like food delivery platform, designed to efficiently manage:

- Users and their profiles
- Restaurant listings and menu management
- Food ordering and tracking
- Reviews and ratings
- Delivery partners and logistics

The schema is built using **SQL** and supports **scalable, normalized relationships** with primary and foreign keys. An **Entity-Relationship (ER) Diagram** provides a clear visual representation of entity relationships.

This project demonstrates a robust, production-ready backend structure for developers and data professionals interested in food-tech applications.

---

## 🚀 Features

### 1. 👥 User Management
- Register and manage user details such as full name, username, email, and registration date.
- Extendable for authentication (email/phone verification).
- Supports account personalization.

### 2. 🍽️ Restaurant and Menu Management
- Add and manage restaurant profiles with cuisine type, contact info, ratings, and location.
- Link menus with restaurants including item name, price, and category (e.g., Starter, Main Course).

### 3. 🧾 Order Tracking
- Record food orders placed by users with timestamps, statuses, and amounts.
- Many-to-many relationship between orders and menu items via the `OrderDetails` table.

### 4. 🌟 Reviews and Ratings
- Users can rate and review restaurants.
- Reviews are tied to both the user and the restaurant with a timestamp and written feedback.

### 5. 🚚 Delivery Management 
- Assign delivery partners to fulfill orders.
- Track delivery routes, optimize logistics, and manage delivery times (planned via `DeliveryPartners` and `DeliveryRoutes` tables).

### 6. 🔗 Scalable Relationships
- Database uses **one-to-many** and **many-to-many** relationships.
- Ensures **referential integrity** using primary and foreign key constraints.

---

## 🗂️ Entity-Relationship Diagram

> 📌 *This section assumes an ER diagram is included in the repository as an image or PDF.*

The ER diagram provides a visual representation of how the entities in the database interact.  
It includes:

- **Users** ←→ Orders, Reviews, Reservations
- **Restaurants** ←→ MenuItems, Orders, Reviews, Reservations
- **Orders** ←→ MenuItems (via OrderDetails)
- **Orders** ←→ DeliveryPartners / Routes *(future extension)*

---

## 🧱 Database Schema Summary

| Table Name        | Description                                      |
|-------------------|--------------------------------------------------|
| `Users`           | Stores user credentials and profiles             |
| `Restaurants`     | Contains restaurant data                         |
| `MenuItems`       | Menu offerings by restaurant                     |
| `Orders`          | Records of food orders                           |
| `OrderDetails`    | Many-to-many link between orders and menu items  |
| `Reviews`         | User-generated feedback and ratings              |
| `Reservations`    | (Optional) Table booking by users                |
| `DeliveryPartners`| (Extension) Information about delivery personnel |
| `DeliveryRoutes`  | (Extension) Tracks delivery paths                |

---

## 🧪 Sample Data Provided

The project includes example `INSERT` statements for:

- Users, Restaurants, and Menus
- Orders and their line items
- Reviews and Reservations

This data helps simulate real-world use cases for testing and demonstration.

---

## 🔍 Example SQL Queries (Use Cases)

- Retrieve top-rated restaurants in Mumbai
- List all menu items under ₹300
- Get all orders placed by a user along with items
- Track pending deliveries
- View reviews submitted in the last week

---

## 🛠️ Tech Stack

- **SQL** (MySQL or PostgreSQL)

---

## 👤 Author

**Atharv Gajanan Shete**  
🎓 BTech CSE | 💼 Data Analyst Aspirant  
🌐 [GitHub - AtharvShete2610](https://github.com/AtharvShete2610)

---


