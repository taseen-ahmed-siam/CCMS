# Cyber Cafe Management System (CCMS)

![PHP](https://img.shields.io/badge/Backend-Core%20PHP-777BB4?style=for-the-badge&logo=php)
![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?style=for-the-badge&logo=mysql)
![Bootstrap](https://img.shields.io/badge/Frontend-Bootstrap-563D7C?style=for-the-badge&logo=bootstrap)
![Status](https://img.shields.io/badge/Status-Maintained-green?style=for-the-badge)

> A comprehensive web-based solution designed to automate and streamline the daily operations of cyber cafes, managing computer terminals, user sessions, and billing efficiently.

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Installation Guide](#-installation-guide)
- [Usage Instructions](#-usage-instructions)
- [Directory Structure](#-directory-structure)

---

## 🚀 Overview

The **Cyber Cafe Management System (CCMS)** serves as a centralized dashboard for administrators to monitor computer usage in real-time. It replaces manual logbooks with a digital tracking system, ensuring accurate billing and historical data retention. The system is built with security and ease of use in mind, utilizing a responsive interface based on the **Sufee Admin** template.

---

## ✨ Key Features

### 🖥️ Administrative Dashboard
- **Real-time Stats:** View total registered users, active computers, and finished sessions instantly.
- **Visual Analytics:** Interactive cards and charts for quick business insights.

### ⚙️ Operational Management
- **Terminal Management:** Add, update, or remove computers with specific location tags (e.g., Gaming Zone, Cabin).
- **Session Tracking:** Generate unique **Entry IDs** for every customer.
- **Automated Billing:** seamless check-in/check-out process with manual fee entry and remark logging.

### 📊 Reporting & Search
- **Date-wise Reports:** Generate detailed activity reports between specific dates for audits.
- **Advanced Search:** Locate user records using Entry ID or Name.

### 🔒 Security
- Secure Admin Authentication (MD5 Encryption).
- Session-based access control.

---

## 🏗️ System Architecture

| Component | Technology Used |
|-----------|-----------------|
| **Frontend** | HTML5, CSS3, Bootstrap 4, JavaScript |
| **Backend** | Core PHP (Procedural) |
| **Database** | MySQL |
| **Server** | Apache (via XAMPP/WAMP) |

---

## 🛠️ Installation Guide

Follow these steps to set up the project locally:

### Prerequisites
- Install **XAMPP**, **WAMP**, or **MAMP**.

### Step 1: Clone or Download
Extract the project files into your server's root directory (e.g., `C:/xampp/htdocs/ccms`).

### Step 2: Database Configuration
1. Open **phpMyAdmin** (`http://localhost/phpmyadmin`).
2. Create a new database named `ccmsdb`.
3. Import the provided SQL file located in the `SQL/` directory.

### Step 3: Connect the Application
Open `includes/dbconnection.php` and configure your credentials:
```php
<?php
$con = mysqli_connect("localhost", "root", "", "ccmsdb");
if(mysqli_connect_errno()){
    echo "Connection Fail".mysqli_connect_error();
}
?>