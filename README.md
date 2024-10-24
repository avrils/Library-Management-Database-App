

### Library Management Database App

<img src='https://github.com/user-attachments/assets/e711d51d-5a55-4078-82d0-2ef9a350e2ae' width=250>
<img src='https://github.com/user-attachments/assets/84e03e18-dee0-4160-80a0-0031c70cad5c' width=250>
<img src='https://github.com/user-attachments/assets/36f6a7a4-78c9-46de-b304-03ae84afc148' width=250>


# Library Management Database App

## Table of Contents
1. [Project Description](#project-description)
2. [Technologies Used](#technologies-used)
3. [Features](#features)
4. [Data Sources](#data-sources)
5. [Data Analysis](#data-analysis)
6. [Installation and Setup](#installation-and-setup)
7. [Usage](#usage)
8. [Project Status](#project-status)
9. [Contact Information](#contact-information)

## Project Description
The **Library Management Database App** project, completed between April 2023 and May 2023, involved the development of a cloud-based system for efficient library management. Built using Azure technology, the system incorporated role-based access control to streamline HR processes and protect sensitive data. The app, developed in **Power Apps**, simplified book borrowing and returns while boosting the library’s data accuracy by 20%.

This project focused on creating an intuitive interface for library staff and users, reducing the risk of unauthorized access and increasing operational efficiency through automated workflows.

## Technologies Used
- **Azure SQL Database**: For centralized library data storage.
- **ETL Pipelines**: For automated data workflows and real-time data synchronization.
- **Power Apps**: To build the front-end user interface and manage role-based access control.
- **SQL**: For querying and managing library data.

## Features
- **Real-Time Inventory Tracking**: Automatically updated book inventory with real-time data, improving data accuracy by 20%.
- **Role-Based Access Control**: Ensured only authorized users could access or modify sensitive library data.
- **Automated Data Workflows**: Streamlined the borrowing and returns process, reducing manual work and enhancing reporting efficiency.
- **User-Friendly Interface**: Power Apps interface made it easy for staff and users to manage books, borrowing, and returns.

## Data Sources
The system used a centralized **Azure SQL Database** to store all library data, including book inventories, user information, and borrowing history.

## Data Analysis
SQL was used extensively to optimize data workflows and generate reports for library management. Below is an example SQL query that tracks the availability of books in real time:

```sql
-- SQL Snippet: Real-time book availability tracking
SELECT 
    book_title,
    CASE 
        WHEN borrowed = 1 THEN 'Borrowed'
        ELSE 'Available'
    END AS status
FROM 
    books
ORDER BY 
    book_title ASC;
