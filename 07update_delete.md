# Update and Delete

## Update
```sql
UPDATE student
SET major = 'Bio'
WHERE major = 'Biology';
```

```sql
UPDATE student
SET major = 'Biochemistry'
WHERE major = 'Biology' OR major = 'Chemistry' ;
```

## Delete
```sql
DELETE FROM student
WHERE student_id = 5;
```
