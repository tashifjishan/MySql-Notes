These constraints can be applied during CREATE TABLE or later via ALTER TABLE:

| Constraint    | Description                    |
|---------------|--------------------------------|
| PRIMARY KEY   | Unique and not null            |
| FOREIGN KEY   | Referential integrity          |
| UNIQUE        | Column must have unique values |
| NOT NULL      | Cannot be NULL                 |
| CHECK         | Enforce a condition            |
| DEFAULT       | Default value                  |


```sql
    CREATE TABLE Users(
        id INT AUTO_INCREMENT primary key,
        name varchar(255) NOT NULL, 
        email varchar(255) NOT NULL UNIQUE,
        password varchar(255) NOT NULL,
    );
```