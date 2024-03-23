---
layout: post
title: Structured Query Language
date: 2024-3-23 15:45 +0100
categories: [Database,Basics]
tags: [database]
---
## Structured Query Language 
- Structured Query Language (SQL)
  - Programming Language used in database
- Cotain three Main Categories
  - Data Definition Language 
  - Data Manipulation Language
  - Data Control Language
## Database Schema
- A schema is a group of related objects in a database.
- There is one owner of a schema who has access to manipulate the structure of any object in the schema
## Data Types
- A data type determines the type of data that can be stored in a database column
- The most commonly used data types are:
  - Alphanumeric
    - stores text data, which includes letters (uppercase and lowercase), numbers (0-9), and special characters. It's often used for names, addresses, or any other kind of information that combines letters, numbers, and symbols.
  - Numeric 
    - numerical data, including integers (whole numbers) and decimals. It's used for storing quantities, measurements, or any other data that represents numbers.
  - Data and Time
    - date and time information. It can represent a specific point in time, a range of dates, or even time intervals.
  - Characters
    - single character, such as a letter, number, symbol, or punctuation mark. It's useful for storing things like initials, codes, or flags.
  - Variable Characters
    - string of characters, similar to alphanumeric data, but with a predefined maximum length. This is useful for storing things like short descriptions, product names, or addresses with a limited number of characters.
  - Integer
    - numbers, positive, negative, or zero. It's used for counting things, representing whole numbers of units, or any other data that doesn't involve decimals.
  - Float 
    - numbers with decimal points. It's used for storing values that can have fractional components, such as measurements, percentages, or monetary amounts.
## Database Constraints
-  Restrictions on Database table or object to help maintain integrity of data.
- Primary Key
 - Not Null
 - Unique
- Not Null
 - This enforces a field to always contain a value which means that you cannot insert a new record, or update a record without adding a value to this field
- Unique Key
  - Ensures that all values in a column are different
- Referential Integrity (Forgin Key)
  - Take Primary key from table A to B as FK
- Check
  - Customize Column