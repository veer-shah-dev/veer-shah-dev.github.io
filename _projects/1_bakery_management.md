---
layout: page
title: Bakery Inventory & Order Management System
description: Modular C-based management system with file-based persistence, customer tracking, and order entry.
img: assets/img/7.jpg
importance: 1
category: Software Engineering
giscus_comments: false
---

## Overview

The **Bakery Inventory & Order Management System** is a modular, text-based desktop application written in **C**. It offers an end-to-end simulation of real-world bakery business operations, handling product cataloging, customer databases, order processing, and persistent file storage.

---

## Key Features

- **Modular Architecture**: Designed using C `struct` data models for `Product`, `Customer`, `Order`, and `UserSession`.
- **File-Based Persistence**: Saves inventory records, order histories, and transaction logs directly to disk using standard C File I/O.
- **Login Authentication**: Secure prompt-driven access control for administrative users.
- **Dynamic Order Processing**: Supports real-time calculation of total order amounts, tax estimations, and inventory stock auto-deduction upon purchase.
- **Search & Filter Capabilities**: Allows quick lookups by Product ID, Customer Name, or Date of Order.

---

## Tech Stack & Concepts Applied

- **Language**: C (ISO C99/C11)
- **Data Structures**: Structs, Dynamic Arrays, Linked File Records
- **Core Concepts**: Control Flow, Modular Functions, Memory Validation, File I/O Streams (`fopen`, `fread`, `fwrite`)
