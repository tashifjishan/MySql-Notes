# Table Creation
Syntax:
```sql
CREATE TABLE table_name (
    column1 datatype constraints,
    column2 datatype constraints,
    ...
);
```
Example:
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    hire_date DATE
);
```
## Key points:

- Define columns with data types (INT, VARCHAR, DATE, etc.).
- Specify constraints like PRIMARY KEY, NOT NULL, UNIQUE, AUTO_INCREMENT.
- Table name must be unique within the database.

# Table Alteration

Used to modify an existing table’s structure.

## Common operations:

### Add column:

```sql
ALTER TABLE table_name
ADD COLUMN column_name datatype constraints;
```
### Modify column:
```sql
ALTER TABLE table_name
MODIFY COLUMN column_name new_datatype new_constraints;
```
### Rename column:
```sql
ALTER TABLE table_name
CHANGE COLUMN old_column_name new_column_name datatype constraints;
```
### Drop column:
```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

# Rename table:
```sql 
RENAME TABLE old_table_name TO new_table_name;
```

# Table Deletion
Drop table (completely removes the table and data):
```sql
DROP TABLE table_name;
Drop multiple tables:
DROP TABLE table1, table2;
```
## Delete all rows but keep the structure:
```sql
TRUNCATE TABLE table_name;
```
### Summary
| Operation     | Command Example                                            | Purpose                         |
|---------------|------------------------------------------------------------|--------------------------------|
| Create Table  | `CREATE TABLE employees (id INT PRIMARY KEY, name VARCHAR(50));` | Create a new table             |
| Add Column    | `ALTER TABLE employees ADD COLUMN age INT;`               | Add a new column               |
| Modify Column | `ALTER TABLE employees MODIFY COLUMN age SMALLINT;`       | Change column datatype/constraints |
| Rename Column | `ALTER TABLE employees CHANGE COLUMN age birth_year INT;` | Rename a column                |
| Drop Column   | `ALTER TABLE employees DROP COLUMN age;`                  | Remove a column                |
| Rename Table  | `RENAME TABLE employees TO staff;`                        | Rename the entire table        |
| Drop Table    | `DROP TABLE employees;`                                    | Remove table and data          |
| Truncate Table| `TRUNCATE TABLE employees;`                                | Remove all data, keep structure|

