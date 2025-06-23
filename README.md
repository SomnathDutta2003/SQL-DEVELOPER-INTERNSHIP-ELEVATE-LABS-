TASK 1: Database Setup and Schema Design – E-Commerce Database

👤 Author: Somnath Dutta

📌 Objective
The objective of this task is to design the structural blueprint of a relational database tailored for an E-Commerce system. The focus is on identifying core entities, their attributes, and relationships—laying the groundwork for an efficient, normalized database schema that supports business operations like product listings, user management, orders, and payments.

🧭 Project Scope
The e-commerce system is expected to support the following features:

Customer registration and login

Product browsing by category

Shopping cart management

Order placement and tracking

Secure payment processing

Administrative control for product and order management

🧱 Database Design Components
1. Entities and Descriptions
Entity	Description
Users	Stores details of customers and administrators.
Products	Contains product information such as name, description, price, and stock.
Categories	Groups products into categories (e.g., Electronics, Clothing).
Orders	Captures details of user purchases including date, status, and total cost.
OrderItems	Links each order to specific products and their quantities.
Payments	Stores payment status, method, and transaction details.
Cart	Temporarily holds selected products before checkout.
Addresses	Manages multiple shipping/billing addresses for users.

2. Attributes (Sample for Key Entities)
Users
User ID

Name

Email

Password (hashed)

Role (Customer/Admin)

Products
Product ID

Product Name

Description

Price

Stock Quantity

Category ID (Reference)

Orders
Order ID

User ID (Customer)

Order Date

Order Status

Total Amount

Payments
Payment ID

Order ID (Reference)

Payment Method (e.g., UPI, Credit Card)

Payment Status

Transaction Date

3. Relationships Overview
One-to-Many:

One User can place many Orders

One Order can have many OrderItems

One Category can contain many Products

Many-to-Many:

Products and Orders (resolved via OrderItems)

One-to-One:

One Order corresponds to one Payment

One User can have one or more Addresses

4. Normalization Approach
To ensure efficient data storage and eliminate redundancy:

1NF: All attributes are atomic (no multi-valued fields).

2NF: Partial dependencies are removed from composite keys (handled using linking tables like OrderItems).

3NF: No transitive dependencies among non-key attributes.
