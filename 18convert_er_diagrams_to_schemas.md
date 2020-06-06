# Convert ER Diagrams To Schemas

## Step 1: Mapping of Regular Entity Types
For each regular entity type create a relation (table) that includes all the simple attributes of that entity.

## Step 2: Mapping of Weak Entity Types
For each weak entity type create a relation (table) that includes all simple attributes of the weak entity.

The primary keys of the weak entity should also include the primary key of the owner of this weak entity.

## Step 3: Mapping of Binary 1:1 Relationship Types
Include one side of the relationship as a foreign key in the other Favor total participation. 

The entity that has total participation should keep the primary key of the other entity as a foreign key in it. 

## Step 4: Mapping of Binary 1:N  Relationship Types
Include the 1 side's primary key as a foreign key on the N side relation (table).

## Step 5: Mapping of Binary N:M Relationship Types
Create a new relation (table) who's primary key is a combination of both entites's primary keys. Also include any relationship attributes.

## Company Database Schema
![Company Database Schema](https://www.mikedane.com/databases/sql/company-relations.png)
Source: [SQL Tutorial by Mike Dane](https://www.mikedane.com/databases/sql/company-relations.png)