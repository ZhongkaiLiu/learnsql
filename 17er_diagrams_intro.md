# ER Diagrams Intro

Entity Relationship (ER)

## Database Schema
The database schema defines
- the tables in the database
- the attributes in tables
  - data types
  - constraints
- relationships between tables

## ER Diagrams
help to convert data storage requirement to the database schema

### Entity
Entity - An object we want to model and store information about

### Primary Key
An attribute that uniquely identify an entry in the database table

### Composite Attribute
An attribute that can be broken up into sub-attributes

e.g
name: first_name + last_name

### Multi-valued Attribute
An attribute that can have more than one value

e.g.
club: club1, club2

### Derived Attribute
An attribute that can be derived from the other attributes

e.g.
has_honors (can be derived from GPA)

### Relationships

#### partial participation
allow part of participation

#### total participation
all members must participlate in the relationship

`Student` --- `Takes` === `Class`

Allow part of students takes class
All class must be taken at least student

### Relationship Attribute
An attribute about the relationship

`Student` --- `Takes` === `Class`
                 |
              `Grade`

e.g. Grade for a student in a class

### Relationship Cardinality
the number of instances of an entity from a relation that can be associated with the relation

types:
- 1 : 1
  - a student can take only 1 class
  - a class can only be taken by 1 student
- 1 : N
  - a student can take N class
  - a class can only be taken by 1 student
- N : M
  - a student can take M class
  - a class can be taken by N student

### Weak Entity
An entity that cannot be uniquely identified by its attributes alone

e.g.
An exam can exist associated with a class
An exam cannot exist without an assciated class

### Identifying Relationship
A relationship that servers to uniquly identify the weak entity

`Class` --- `Has` === `Exam`

e.g.n
A class has an exam

## ER Diagram Example

![Company ER ](https://www.mikedane.com/databases/sql/company-erd.png)
Source: [SQL Tutorial by Mike Dane](https://www.mikedane.com/databases/sql/company-erd.png)





