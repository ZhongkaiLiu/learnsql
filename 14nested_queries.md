# Nested Queries

## Nested queries

find names of all employees who have sold over 30,000 to a single client

```sql
SELECT employee.first_name, employee.last_name
FROM employee
WHERE employee.emp_id IN (
    SELECT works_with.emp_id
    FROM works_with
    WHERE works_with.total_sales > 30000
);

-- use JOIN to get the same result, NOT the best method
SELECT employee.first_name, employee.last_name
FROM employee
JOIN works_with
ON employee.emp_id = works_with.emp_id
WHERE works_with.total_sales > 30000;
```

find all clients who are handled by the branch that Michael (employee_id = 102) manages

```sql
SELECT client.client_name
FROM client
WHERE client.branch_id = (
    SELECT branch.branch_id
    FROM branch
    WHERE branch.mgr_id = 102
    LIMIT 1
);
```

The inner query will be executed first