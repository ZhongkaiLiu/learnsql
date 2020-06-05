# Functions

## COUNT()
find the number of employees
```sql
SELECT COUNT(emp_id)
FROM employee;
```

COUNT() will count number of rows that has value (i.e. NOT NULL)

## AVG()
find the average of all employee's salaries
```sql
SELECT AVG(salary)
FROM employee
```

## SUM()
find the sum of all employee's salaries
```sql
SELECT SUM(salary)
FROM employee
```

## GROUP BY
find the total sales of each salesman
```sql
SELECT emp_id, SUM(total_sales)
FROM works_with
GROUP BY emp_id
```