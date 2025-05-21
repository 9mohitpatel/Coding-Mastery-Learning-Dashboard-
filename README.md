# 🎓 Coding Mastery - Minor Project (Java Web Application)

A dynamic educational platform built using Java Servlets and JSP to manage user registrations, course enrollments, and contact messaging. This project demonstrates core concepts of full-stack Java web development using the MVC pattern.

---

## 🌐 Live Preview (Optional)

> [Optional link to your deployed project on localhost or hosting platform]

---

## 📌 Table of Contents

- [📖 Overview](#-overview)
- [🧰 Technologies Used](#-technologies-used)
- [✨ Features](#-features)
- [📁 Project Structure](#-project-structure)
- [🛠️ Setup Instructions](#️-setup-instructions)
- [🧬 MySQL Database Schema](#-mysql-database-schema)
- [📄 How to Add New Servlets](#-how-to-add-new-servlets)
- [🖼️ Screenshots](#-screenshots)
- [🛣️ Future Enhancements](#️-future-enhancements)
- [📞 Contact](#-contact)
- [📜 License](#-license)

---

## 📖 Overview

This project is a **minor project for Computer Science Engineering** students focusing on:

- Building dynamic web applications using **Java EE**
- Managing backend logic with Servlets
- Integrating **MySQL** database for persistence
- Using JSPs for view rendering

---

## 🧰 Technologies Used

- **Java** (JDK 8+)
- **Servlets & JSP** (Java EE)
- **HTML, CSS, JavaScript**
- **Apache Tomcat** (v8+)
- **MySQL Database**
- **NetBeans IDE**
- **JDBC (MySQL Connector)**

---

## ✨ Features

- 🔐 **User Authentication** (Admin & User)
- 📝 **Course Enrollment** form with payment tracking
- 📬 **Contact Form** with timestamped messages
- 📦 MVC-based architecture (Servlets as Controllers)
- 🔌 MySQL Database integration
- ⚙️ Session Tracking

---

---

## 🛠️ Setup Instructions

### 1. Prerequisites

- Install JDK (Java 8 or above)
- Install NetBeans IDE
- Download and configure **Apache Tomcat**
- Install **MySQL Server**

### 2. Project Setup in NetBeans

- Open NetBeans → `File > Open Project` → Select folder
- Add MySQL JDBC connector via `Project > Properties > Libraries > Add JAR/Folder`
- Configure Tomcat via `Tools > Servers > Add Server`

---

## 🧬 MySQL Database Schema

Run this in **MySQL CLI**, **phpMyAdmin**, or **Workbench**:

```sql
CREATE DATABASE minorproject;
USE minorproject;

CREATE TABLE users (
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    password VARCHAR(100),
    role ENUM('user', 'admin')
);

CREATE TABLE enrollment (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    mobile VARCHAR(15) NOT NULL,
    email VARCHAR(100) NOT NULL,
    course VARCHAR(100) NOT NULL,
    payment DECIMAL(10, 2) NOT NULL
);

CREATE TABLE contact_messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(150) NOT NULL,
    subject VARCHAR(200) NOT NULL,
    message TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

✨ Features
🔐 User Management
User Registration & Login
Register new users with name, email, password, and role.

Role-based Access Control
Two roles supported: user and admin.

📚 Course Enrollment
Dynamic Enrollment Form
Users can enroll by submitting their name, email, mobile number, course name, and payment amount.

Data Stored in MySQL
Enrollments are stored in the enrollment table with auto-incremented IDs.

📬 Contact Form System
Contact Us Page
Users can send inquiries through a contact form.

Backend Storage
All messages are saved to the contact_messages table with a timestamp.

💾 MySQL Database Integration
All dynamic data is stored and retrieved from a MySQL database using JDBC.

Database tables include: users, enrollment, contact_messages.

🖥️ Admin Access (Planned or Implemented)
Admin Login
Special access to view or manage enrollments and contact submissions.

Future Dashboard Support
Easily extendable for admin dashboards and analytics.

🔗 Session Management
Tracks user sessions after login for personalized access.

Used to restrict page access without re-login.

📄 Servlet + JSP Architecture
MVC Pattern
Clean separation of logic (Servlet), presentation (JSP), and data access (DAO).

Reusable Components
Easily extendable design for additional features like quizzes or course listings.

⚙️ Modular Codebase
DAO Layer handles all DB logic.

Servlet Layer handles HTTP requests and form submissions.

JSPs used for rendering user-friendly pages.

🎯 Fully Functional Educational Workflow
From user registration to course enrollment and messaging, the complete flow mimics real educational platforms.



