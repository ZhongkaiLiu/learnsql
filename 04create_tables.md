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

-- show schema of table
DESCRIBE student; 
```

## Set Primary Key
```sql
CREATE TABLE student (
    student_id INT,
    name VARCHAR(20),
    major VARCHAR(20),
    PRIMARY KEY(student_id)
);
```

## Set Foreign Key While Creating Table
```sql
CREATE TABLE branch (
    branch_id INT PRIMARY KEY,
    branch_name VARCHAR(40),
    mgr_id INT,
    mgr_start_date DATE,
    FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
);
```

## Set Foreign Key After Creating Table
```sql
ALTER TABLE employee
ADD FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE SET NULL;
```

## Delete table
```sql
DROP TABLE student;
```

## Add / Delete column
```sql
ALTER TABLE student 
ADD gpa DECIMAL(3, 2);
```

```sql
ALTER TABLE student 
DROP COLUMN gpa;
```