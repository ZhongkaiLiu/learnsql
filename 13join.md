# Join

## Inner Join
find all branches and the names of their managers
```sql
SELECT employee.emp_id, employee.first_name, branch.branch_name
FROM employee
JOIN branch
ON employee.emp_id = branch.mgr_id;
```
Returned table only has the rows that match `employee.emp_id = branch.mgr_id`

## Left Join
```sql
SELECT employee.emp_id, employee.first_name, branch.branch_name
FROM employee
LEFT JOIN branch
ON employee.emp_id = branch.mgr_id;
```
Returned table has all rows in the left table,
when NOT match `employee.emp_id = branch.mgr_id`, the columns in right table will be NULL

## Right Join
```sql
SELECT employee.emp_id, employee.first_name, branch.branch_name
FROM employee
RIGHT JOIN branch
ON employee.emp_id = branch.mgr_id;
```
Returned table has all rows in the right table,
when NOT match `employee.emp_id = branch.mgr_id`, the columns in left table will be NULL