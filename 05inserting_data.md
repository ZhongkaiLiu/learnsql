# Inserting Data

## insert row
```sql
INSERT INTO student VALUES(1,"Jack","Biology");
INSERT INTO student VALUES(2,"Kate","Sociology");

-- only insert with part of columns
INSERT INTO student(student_id, name) VALUES(3, "Claire");
```