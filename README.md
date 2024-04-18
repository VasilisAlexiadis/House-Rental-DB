# House-Rental-DB


# Overview
This repository contains the SQL code and schema for a relational database management system (RDBMS) designed to manage house rental data. It includes scripts for creating tables, inserting data, and querying a PostgreSQL database. This system is built to handle different entities such as owners, apartments, tenants, rentals, and reviews, making it an integral tool for rental property management.

# Features
Database Setup: Scripts to create tables with primary keys, foreign keys, unique, check, and referential integrity constraints.
Data Integrity: Comprehensive constraints to ensure data quality, including checks for valid postal codes and email formats.
Utility Scripts: Includes sequences for auto-incrementing primary keys and utility queries for database maintenance.
Sample Data Insertion: Pre-filled scripts to insert initial data into the database for testing and development purposes.
Query Examples: A wide variety of SQL queries for common use cases, such as finding tenants by country or sorting apartments by price.
File Descriptions
schema.sql - Contains all SQL commands for setting up the database schema, including table creations and constraints.
inserts.sql - Pre-populated data insertion commands to help set up your database with initial data.
queries.sql - Example SQL queries for interacting with the database, including data retrieval and reporting tasks.

# Setup Instructions
Database Creation
Ensure that PostgreSQL is installed on your machine.
Create a new database named HouseRentalDB:
sql
Copy code
CREATE DATABASE HouseRentalDB;
Connect to the database using:
bash
Copy code
psql -d HouseRentalDB
Schema Setup
Run the schema.sql script to set up the database schema:
bash
Copy code
\i path/to/schema.sql
Data Insertion
Populate the database with initial data using:
bash
Copy code
\i path/to/inserts.sql
Running Queries
You can start running queries listed in queries.sql to interact with the database:
bash
Copy code
\i path/to/queries.sql
Usage Examples
Here are some example operations you can perform with the provided scripts:

Finding Apartments by City:
sql
Copy code
SELECT * FROM Apartment WHERE apa_city = 'Thessaloniki';
List Rentals for a Specific Tenant:
sql
Copy code
SELECT * FROM Rental WHERE t_id = 100001;
Check Reviews for Apartments:
sql
Copy code
SELECT apa_id, AVG(rv_rating_stars) as average_rating FROM Review GROUP BY apa_id;
Contributions
Contributions are welcome! If you have improvements or bug fixes, please open a pull request with a clear description of changes.

# License
This project is available under the MIT License. Feel free to use and modify the code as per your needs with proper attribution.

