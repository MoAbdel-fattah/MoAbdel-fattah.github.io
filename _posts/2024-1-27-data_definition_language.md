---
layout: post
title: Data Definition Language
date: 2024-1-27 10:16 +0200
categories: [SQL]
tags: [sql,database]
---

# DDL : Data Definition Language
## DDL Processes :
### 1- Create :  
#### - Database
```sql
create database database_name;
```
#### - Table
```sql
create table table_name (
column1 datatype,
column2 datatype,
column3 datatype,
...........
);
```

### 2- Drop
- Delete Database
```sql
drop database database_name;
```
- Delete Table
```sql
drop table database_name;
```

### 3- Alter
- Change structure of table
  - For add column:
  ```sql
  ALTER TABLE table_name ADD COLUMN column_name;
  ```
  - for delete column:
  ```sql
  ALTER TABLE table_name DROP COLUMN column_name;
  ```
- Change specfic property on Database

## Column Data Types :
### 1-String
- char : for Fixed length
- varchar : for dynamic size 
- text : for more size
- enum : for specific value
- set  : for selection value 
### 2-Numeric
- int : store number
- float : store decimal number
### 3-Date/Time
- date
- time
- datetime
- timestamp
- year