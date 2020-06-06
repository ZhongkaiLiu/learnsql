# Union

## Union
find a list of all clients & branch suppliers' names
```sql
SELECT client_name, client.branch_id
FROM client
UNION
SELECT supplier_name, branch_supplier.branch_id
FROM branch_supplier;
```

The numbers of columns in two SELECT statements must be equal, and should be similar data type