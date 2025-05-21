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



