# Create Tables

## Data types
- INT
  - whole number
- DECIMAL(M, N)
  - M digits, N digits after decimal point
- VARCHAR(L)
  - string of length L
- BLOB
  - binary large object, stores large data, e.g. image
- DATE
  - 'YYYY-MM-DD'
- TIMESTAMP
  - 'YYYY-MM-DD HH:MM:SS'

## Create table

```sql
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);

DESCRIBE student; 
```

## Delete table
```sql
DROP TABLE student;
```

## Add / Delete column
```sql
ALTER TABLE student ADD gpa DECIMAL(3, 2);

ALTER TABLE student DROP COLUMN gpa;
```