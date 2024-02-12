---
layout: post
title: Data Manipulation Language
date: 2024-1-27 19:39 +0200
categories: [SQL]
tags: [sql,database]
---
## DML Process:
### 1- Insert
```sql
INSERT INTO 'table_name'('col1','col2') VALUES ('val 1','val 2');
```
```sql
INSERT INTO 'table_name' SET 'col1' = 'val1' , 'col2' = 'val2' ;
```

### 2- Update
```sql
UPDATE 'table_name' SET 'col1' = 'val1' , 'col2' = 'val2' WHERE 'col' = 'value' ;
```

### 3-  Delete
```sql
DELETE FROM 'table_name' SET  WHERE 'col' = 'value' ;
```