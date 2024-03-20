---
layout: post
title: Entity Relationship Diagram 
date: 2024-3-16 00:00 +0000
categories: [Database,Basics]
tags: [database]
---
## Entity Relationship Modeling
- Identifies infromation required by the business by displaying the relevant entities and relationships between them.
### Entity
- Is a thing in the real world with an independent existence.
- Take a Rectangle Shape in ERD
- Is descriped by set of attribute.
- Strong entity : Can have unique identifier or unique attributes.
- Weak Entity : An entity that does not have a key attribute , must be fully dependent on another entity.
#### Attributes
- Take a Circle shape in ERD
- Single/Simple Attribute : Attributes that are not divisble and have a single value for a particular entity instance.(Example/ID,SSN)
- Multi-valued Attribute :  Has a set of values for the same entity instance , (Example/Phone_number)
- Composite Attribute : Can be divided into smaller subparts (Example/Area_Zone)
- Derived Attribute : can be calculated from another attribue or entity(Example/Age)
- Candidate Key : when an entity type has more than one key.those are candidate keys.
## Relationship 
- A relationship is a connection between entity classes
- Every relationship in database must have :
  - Degree
  - Cardinality Ratio
  - Particioation
### Degree Of Relationship
- Is The Number of participating entity.
- Take Diamond Shape In ERD
- Binary Relationship : Between two entities.
- Unary / Recursive Relationship : Between entity and itself(Example/Supervisor)
- Ternary Relationship : Between three entities.
### Cardinality Ratio
- Specifies the maximum number of relationship.
#### Types of Cardinality Ratio
1. one-to-one
2. one-to-many
3. many-to-many
## Notations in ERD
1. M (Many): 
- This typically refers to a many-to-many relationship (often denoted as M:N). In a many-to-many relationship, multiple instances of one entity are related to multiple instances of another entity. 
- For example, consider a scenario where students can enroll in multiple courses, and each course can have multiple students. This relationship is represented by an associative entity connecting the two main entities: Student and Course12.
2. K (Key): 
- In ERDs, a key is a unique identifier for an entity. It helps distinguish individual occurrences of an entity. There are different types of keys:
  - Primary Key: 
    - A primary key uniquely identifies each record in an entity. 
    - For instance, in a Student entity, the student ID could be the primary key.
  - Foreign Key: 
    - A foreign key establishes a link between two entities. It refers to the primary key of another entity. 
    - For example, if we have a Course entity, the course ID could be a foreign key linking it to the Student entity1.
3. N (Number): 
- In the context of relationships, “N” often represents the cardinality of the relationship. 
- It indicates how many instances of one entity are related to another. 
- Here are some common cardinalities:
   - 1:N (One-to-Many): 
     - One instance of an entity is related to multiple instances of another entity. 
     - For example, a customer can place multiple orders, but each order belongs to only one customer.
   - N:M (Many-to-Many): 
     - Multiple instances of one entity are related to multiple instances of another entity. 
     - As mentioned earlier, this is represented by an associative entity. For instance, a student can attend multiple classes, and each class can have multiple students345.