# Timeless Cuisine: Restaurant Ordering and Inventory System

An Information Systems Analysis and Design (ISAD) project covering restaurant ordering, payments, raw-material management, and reporting. The deliverables include process models, UML diagrams, Figma interface designs, and a proposed system architecture.

- **Design tools:** Draw.io and Figma
- **Project scope:** Academic case study, system analysis, and design

## Project Overview

Timeless Cuisine is a restaurant case study with dine-in and takeaway services. Customers order through tablets at their tables, while staff handle payments, purchasing, stock records, and menu management.
Our group examined how these activities could work together in one system, documented the requirements and use cases, and designed the process models, UML diagrams, and interfaces.

## Problem Identification

The Fishbone Diagram groups the causes of inefficient restaurant operations into five areas:

- **Suppliers:** A limited supplier list and dependence on one supplier restrict purchasing options.
- **Recording and purchasing:** Staff enter stock records manually, and raw-material purchasing is not handled automatically or in real time.
- **Systems and integration:** Sales, purchasing, and inventory are disconnected. Low stock is not detected reliably, and stock and menu availability are not kept in sync with ordering.
- **Ordering:** Customers cannot add order notes or choose dine-in and takeaway separately for individual items.
- **Reporting and management:** Profit and loss reports, best-selling menu information, and a central dashboard are not available automatically.

<img width="1017" height="636" alt="image" src="https://github.com/user-attachments/assets/fe33827a-bf99-4de2-9f27-fd9511d2648c" />


## Users and Main Workflows

| User | Main workflows |
| --- | --- |
| **Customer** | Browse the menu, enter order preferences, place an order, and make a payment. |
| **Cashier** | Check order details, process payments, and issue receipts. |
| **Warehouse staff** | Request raw materials and record their receipt and usage. |
| **Purchasing staff** | Review warehouse requests and arrange raw-material purchases. |
| **Administrator** | Manage menu entries and prepare sales and profit and loss reports. |

Management receives the reports to review restaurant performance. Suppliers and the bank appear as external entities in the process models.
The ordering requirements include additional notes and a dine-in or takeaway choice for each item. For dine-in customers, the case describes payment at the cashier after the meal, using cash, a debit card, a credit card, or QRIS.
Warehouse requests lead to purchasing and goods receipt. Received materials increase stock, while recorded usage reduces it. The design aims to share stock information with ordering and reporting.

## Process and Data Modelling

The Context Diagram shows the system boundary and information exchanged with customers, the cashier, warehouse and purchasing staff, administrators, management, suppliers, and the bank.

The DFD Level 0 divides the system into four processes:
1. **Ordering:** Capture customer orders and provide order details to the cashier.
2. **Payment:** Process payment information and confirmation.
3. **Raw-material management:** Handle purchase requests, goods receipt, and stock information.
4. **Reporting:** Provide sales and profit and loss information to management.

<img width="510" height="590" alt="image" src="https://github.com/user-attachments/assets/c8b5a73c-8594-4d91-ae3a-9bd6bacf15a7" />


## Object-Oriented Analysis and Design

| Model | What it covers |
| --- | --- |
| **Use Case Diagram** | Ten use cases across customer, cashier, warehouse, purchasing, and administrator roles. |
| **Use Case Descriptions** | Scenarios, actors, triggers, preconditions, postconditions, activity flows, and exceptions for all ten use cases. |
| **Class Diagram** | Customers, staff, menus, raw materials, suppliers, and forms for orders, order details, payments, purchases, and purchase details. |
| **Sequence Diagrams** | Five selected workflows: ordering, customer payment, recording raw-material usage, sales reporting, and profit and loss reporting. |
| **Activity Diagrams** | Five selected workflows: ordering, cashier payment processing, raw-material requests, purchasing, and usage recording. |
| **State Transition Diagrams** | State changes for customer orders and raw-material purchasing. |

<img width="971" height="639" alt="image" src="https://github.com/user-attachments/assets/10231a44-d842-4b1e-840e-6f4d46bbd5bd" />

The other diagrams are available in this repository or through the Draw.io link in the Project Links section below.

## User Interface Design

The Figma designs show the main inputs, confirmations, and outputs for restaurant users:

- **Customer:** Menu browsing, service-type selection, order preferences, order confirmation, payment selection, and payment status.
- **Cashier:** Order totals, payment processing, and receipts.
- **Warehouse and purchasing staff:** Raw-material requests, receipt and usage records, purchase confirmation, and purchase status.
- **Administrator and management:** Menu entry, reporting forms, and a dashboard showing profit figures, sales trends, and popular menu items.

The values shown in the dashboard and transaction screens are examples used in the mockups.

<img width="1118" height="693" alt="Preview" src="https://github.com/user-attachments/assets/413d8aac-5ac4-462e-aba9-2f6f7dd824d2" />
<img width="885" height="610" alt="Dashboard" src="https://github.com/user-attachments/assets/1fbe83a9-c4c3-4d28-9a84-e9274715c785" />

## Project Links

- **Figma:** [View the interface designs](https://www.figma.com/design/LjD7iCdOtjCjUJo0Cq5wiM/Projek-ISAAD-Lec-Kelompok-3?node-id=0-1)
- **Draw.io:** [View the diagram source](https://app.diagrams.net/#G172ckzSYiWJ--IhQ8w4iwNVikchRklC2A#%7B%22pageId%22%3A%22r5EgvA7yNDVd6BKgMjM3%22%7D)
  
## Proposed System Architecture

The project proposes a three-tier client/server architecture. Customer and staff devices act as clients, sending requests to a server that processes business rules and accesses the database.

| Tier | Responsibility |
| --- | --- |
| **Presentation** | Interfaces for ordering, payment, stock recording, purchasing, menu management, and viewing reports. |
| **Application** | Business logic for order totals, payment processing, stock updates, and reporting. Java is proposed for this tier. |
| **Data** | Storage for menu, order, payment, raw-material, supplier, and purchase records. MySQL is proposed for this tier. |

This separation gives each tier a clear responsibility for future development and maintenance. The project scope is system analysis, interface design, and architecture planning.

## Contributors

- Nacito Florisen Astari
- Ahmad Alfakhridzi Mirza
- Putu Gde Wibi Adhidarma
- Kepin Simatupang
