# Triggers

## Create trigger
```sql
CREATE TRIGGER trigger_name
BEFORE INSERT ON employee
FOR EACH ROW 
BEGIN
    INSERT INTO log VALUE('add new employee');
END
```

- This trigger will add a log record into table `log`, when insert a new record into `employee`.

## NEW
```sql
CREATE TRIGGER trigger_name2
BEFORE INSERT ON employee
FOR EACH ROW 
BEGIN
    INSERT INTO log VALUE(NEW.first_name);
END
```

- `NEW.first_name` access the new row that inserted

## IF, ELSE
```sql
CREATE TRIGGER trigger_name3
BEFORE INSERT ON employee
FOR EACH ROW 
BEGIN
    IF NEW.sex = 'M' THEN
        INSERT INTO log VALUES('add a male employee');
    ELSEIF NEW.sex = 'F' THEN
        INSERT INTO log VALUES('add a female employee');
    ELSE
        INSERT INTO log VALUES('add an employee');
    END IF;
END
```

## Change Delimiter

```sql
DELIMITER $$
```

change delimiter to `$$` instead of `;`

```sql
DELIMITER ;
```

change delimiter back to `;`