# Wildcards

## LIKE
find any client's who are an LLC
```sql
SELECT *
FROM client
WHERE client_name LIKE '%LLC';
```

find any employee born in Octorber
```sql
SELECT *
FROM employee
WHERE birth_date LIKE '____-10%'
```

## Patterns

% = any number of characters
_ = one character