# More Basic Queries

## Change the columns name in returned result
```sql
SELECT first_name AS forename, last_name AS surname
FROM employee;
```

## Find out all different genders
```sql
SELECT DISTINCT branch_id
FROM employee;
```