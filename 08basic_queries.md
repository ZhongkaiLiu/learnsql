# Basic Queries

## Retrieve all columns
```sql
SELECT * FROM student;
```

## Retrieve certain columns
```sql
SELECT name, major
FROM student;
```

## Order by one columns
### Ascending
```sql
SELECT name, major
FROM student
ORDER BY name ASC;
```
by default, it is ordered by ascending

### Descending
```sql
SELECT name, major
FROM student
ORDER BY student_id DESC;
```

### Order by multiple columns
```sql
SELECT name, major
FROM student
ORDER BY major, student_id DESC;
```

## Limit number of rows
```sql
SELECT name, major
FROM student
ORDER BY major, student_id
LIMIT 3;
```

## Filtering
```sql
SELECT name, major
FROM student
WHERE major = 'Biology'
ORDER BY major, student_id
LIMIT 3;
```

## Comparators and Logic Operators
equal =
not equal <>
larger than >
less than <
larger and equal >=
less and equal <=
logic and, AND
logic or, OR
logic not, NOT

## IN
```sql
SELECT *
FROM student
WHERE name IN ('Claire', 'Kate', 'Mike');
```

