# 🅿️ ConvenientParking (LBParking)

**ConvenientParking** is a comprehensive web-based Parking Management System built with **Java Spring Boot**. The system streamlines parking spot rentals for customers while providing robust administrative tools for employees and managers.

---

## 📌 Overview
The application follows a **layered architecture pattern** and utilizes a RESTful API structure to manage parking operations, contracts, and revenue statistics efficiently.

### 🛠 Technologies Used
*   **Backend:** Java 17+, Spring Boot, Spring Data JPA
*   **Build Tool:** Maven
*   **Database:** MySQL (or compatible RDBMS)
*   **Utility:** Lombok, RESTful API
*   **Reporting:** Excel/PDF Exporting

---

## 🚀 Features

### 👤 Customer (USER)
- **Account:** Register and verify via email; PIN-based password recovery.
- **Vehicles:** Register vehicle details (plate number, type, and images).
- **Wallet:** Top-up account balance for seamless rentals.
- **Rentals:** 
  - Rent by **Hour, Day, Month, or Year**.
  - Multiple parking spots per contract.
  - Automatic price calculation based on duration and vehicle type.

### 👨‍💼 Employee (EMPLOYEE)
- **Analytics:** Revenue statistics filtered by date range, month, or year.
- **Visuals:** Bar chart visualizations for package usage and spot revenue.
- **Reporting:** Export detailed reports to **Excel or PDF**.

### 🛠 Administrator (ADMIN)
- **User Management:** Assign roles (**USER, EMPLOYEE, ADMIN**), lock/unlock accounts.
- **Pricing:** Dynamically modify pricing and rental configurations.

---

## 🏗 System Architecture

### Layer Responsibilities
1.  **Controller Layer:** Handles HTTP requests, validates input, and returns JSON.
2.  **Service Layer:** Contains core business logic and processes transactions.
3.  **Repository Layer:** Communicates with the database via JPA CRUD operations.
4.  **Entity Layer:** Maps database tables using JPA annotations.

### 🗂 Project Directory Structure
```text
src/main/java/com/example/convenientparking
├── Config          # Security & configuration classes
├── Constants       # System constant values
├── Controllers     # REST Controllers (API layer)
├── Entities        # JPA Entity classes
├── Repositories    # Spring Data JPA repositories
├── Services        # Business logic layer
└── ConvenientParkingApplication.java

