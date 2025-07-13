- Show all databases=> **SHOW DATABASES**;
- Create a new database => **CREATE DATABASE dbname**;
- Use a database=>	**USE dbname**;
- Delete a database=> **DROP DATABASE dbname**;


| Action                     | Command                                                                  |
|---------------------------|---------------------------------------------------------------------------|
| Show all tables in DB     | `SHOW TABLES;`                                                            |
| Create a table            | `CREATE TABLE tablename (id INT, name VARCHAR(50));`                      |
| Show table structure      | `DESCRIBE tablename;` **OR** `SHOW COLUMNS FROM tablename;`              |
| Rename a table            | `RENAME TABLE oldname TO newname;`                                       |
| Add a new column          | `ALTER TABLE tablename ADD columnname DATATYPE;`                         |
| Modify a column           | `ALTER TABLE tablename MODIFY columnname NEW_DATATYPE;`                  |
| Change column name/type   | `ALTER TABLE tablename CHANGE oldname newname DATATYPE;`                 |
| Drop a column             | `ALTER TABLE tablename DROP COLUMN columnname;`                          |
| Delete a table            | `DROP TABLE tablename;`                                                  |

