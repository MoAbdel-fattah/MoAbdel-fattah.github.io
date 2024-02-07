---
layout: post
title: General Knowledge in Database
date: 2024-2-7 14:57 +0200
categories: [Database]
tags: [database]
---
## Database concepts:
- before the database,there was something called file-based system , this system relay on we have a group of programs and application offer some services, each program definded and manged in has way,and if company have a few department and each department have has own file-based system,  we will have a lot of limitations.
### Limitations Of File Based System
- Seperation and Isolation of data.
- Duplication of data.
- Program Data Dependence.
- Incompatible file formats.
### Concepts Of Database:
- Database: A collection of related data.
- Database Management System(DBMS): A Software package/system to facilitate the creation and maintenance of a computerized database.
## Database systems ,  Main components:
- Database System: The DBMS software together with the data itself.Sometimes, the application are also included.
- Metadata: Stored Database Definition.
- DBMS = Software to process queries + Software to access stored data. 
### Database Systems Advantages:
- Controlling Redundancy.
- Restricting Unauthorized Access.
- Sharing Data.
- Enforcing Integrity Constraints.
- Inconsistency can be avoided.
- Backup and Recovery Data.
### Database Systems Disadvantages:
- Needs expertise to use.
- Expensive.
## Database Users:
### System Analysts:
- Business analysis and requirement gathering.
### Database Designer:
- Create database design(Conceptual Schema).
### Database Administrator:
- Install DBMS.
- Create DB schema and populate.
- Create Users and authorize access to DB.
- Maintain DB performance.
### Application Programmar:
- Develop, test and debug application. 
## DBMS Architecture:
### External Schema:
- There is many external schema the DBMS.
- They are concerned with what data the user will see and how the data will be presented to the users.
### Conceptual Schema:
- Also called logical model
- They are concerd with what is represented
### Physical Schema:
- Also called physical model.
- Represent the allocation of data in disk and size of it.
## Data Models:
### Logical Model:
- Conceptual model that provide concepts that are close to the way many users perceive data,entities,attributes and relationships.
### Physical Model:
- Describe how data stored , access path needed to access and search for data.
## Mappings
- It is the processes of transforming requests and results between levels.
## Centralized Database Environment:
### Mainframe environment:
- A group of pcs connected in one machine that contain database server and application server using dummy terminals.
- Pcs just show the data and the application not setup in it
- These terminals do not make any processing,just make some requests.
- The performance is very slow.
- Database and application layer has single point of failure
### Client/Server environment:
- Contain database servers and thick client.
- Thick Client have the application and the application locally.
- High Cost for maintunce and support
- Application layer is not a single point of failure
- Database is a single point of failure
### Internet Computing environment:
- Also called Three-tier architecture or N-tier architecture and that depends on how many application server on it.
- There is a three compnents in it (Database server , Application Server , Thim Client).
- Application layer is  a single point of failure.
- Lower Cost for maintunce and support.
- Application Server is a single point of failure.
## Distributed Database Environment:
- Support high availablitiy of database.
- Database is a not single point of failure 
- There is no downtime
- High Cost 
- There is a two way to make distribution of database :
-- Replication.
-- Fragmentation.
### Replication:
- It is simple as we make a copy and paste for database.
- There is two way to make replication for the database:
#### Partial Replication:
- Copy only part of database to anthor server.
#### Full Replication:
- Copy all of database to anthor server and the two servers working back to back.
- If one of two servers stop the all of requests will be routed on anthor server
### Fragmentation:
- As we make a cut and paste for the database.
#### Horizontal Fragmentation:
- Devide database into fragments and this fragments can be horizontal as a group of recoreds.
#### Vertical Fragmentation:
- Devide database into fragments and this fragments can be vertical as a group of columns.
#### Hybird Fragmentation:
- Devide database into fragments and this fragments can be vertical and horizontal as a group of columns and recoreds.