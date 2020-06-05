# Constraints

## NOT NULL, UNIQUE, AUTO_INCREMENT
```sql
CREATE TABLE student (
    student_id INT AUTO_INCREMENT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) UNIQUE,
    PRIMARY KEY(student_id)
);
```

## DEFAULT
```sql
CREATE TABLE student (
    student_id INT,
    name VARCHAR(20),
    major VARCHAR(20) DEFAULT 'undecided',
    PRIMARY KEY(student_id)
);
```

## Composite key
```sql
CREATE TABLE student (
    student_id INT,
    name VARCHAR(20),
    major VARCHAR(20) UNIQUE,
    PRIMARY KEY(student_id, name)
);
```
