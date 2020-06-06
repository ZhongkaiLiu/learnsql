# On delete

when set foreign key, we need to specify how it should behave when the original key is deleted
## ON DELETE SET NULL
```sql
CREATE TABLE branch (
    branch_id INT PRIMARY KEY,
    branch_name VARCHAR(40),
    mgr_id INT,
    mgr_start_date DATE,
    FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
);
```

```sql
FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
```

- This set `mgr_id` as foreign key, which refers to `emp_id` in table `employee`.
- When `emp_id` is deleted in table `employee`, it will become `NULL`.

## ON DELETE CASCADE
```sql
CREATE TABLE branch_supplier (
    branch_id INT,
    supplier_name VARCHAR(40),
    supply_type VARCHAR(40),
    PRIMARY KEY(branch_id, supplier_name),
    FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE CASCADE
);
```
- branch_id can be both primary key and foreign key in this table
- When `branch_id` deleted in table `branch`, it will delete the row
- Since `branch_id` is also the primary key, it cannot be `NULL`
