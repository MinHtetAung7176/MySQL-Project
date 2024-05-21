# SQL Project Documentation

## Table of Contents
- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [SQL Queries](#sql-queries)
  - [Query 1](#query-1)
  - [Query 2](#query-2)
  - [Query 3](#query-3)
  - [Query 4](#query-4)
  - [Query 5](#query-5)
  - [Query 6](#query-6)
  - [Query 7](#query-7)
  - [Query 8](#query-8)
  - [Query 9](#query-9)
  - [Query 10](#query-10)
- [Usage](#usage)
- [Author](#author)

## Introduction
This project contains a set of SQL queries designed to extract and manipulate data from a database related to a faculty and course offering system. The queries perform various tasks such as selecting specific records, joining tables, grouping data, and applying conditions.

## Project Structure
The project consists of a single file containing all the SQL queries:
- `queries.sql`: Contains all the SQL queries listed and explained below.

## SQL Queries

### Query 1
```sql
SELECT 
  FacFirstName AS 'FirstName', 
  FacLastName AS 'LastName', 
  FacCity AS 'City', 
  FacSalary AS 'facsalary', 
  ROUND(FacSalary - (FacSalary * 0.05)) AS 'DecreasedSalary', 
  FacHireDate AS 'HireDate'
FROM FACULTY
WHERE YEAR(FacHireDate) < 1998;
