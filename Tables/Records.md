# Insert data
```sql
INSERT INTO users (name, email, age)
VALUES ('Alice Smith', 'alice@example.com', 30);
```

# Update (Modify existing data)
```sql
UPDATE users
SET name = 'Alice Johnson', age = 31
WHERE id = 1;
```


# Delete (Remove data)
```sql
DELETE FROM users
WHERE id = 1;
```