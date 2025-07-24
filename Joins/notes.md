# 🧠 Why Do We Need Multiple Tables in Databases?
In real-world applications, storing everything in one table leads to redundancy and inconsistency. Here's why multiple tables are necessary:

✅ Benefits of Using Multiple Tables
| Reason                 | Explanation                                                                 |
|------------------------|------------------------------------------------------------------------------|
| Avoid Data Redundancy  | No repetition of data. E.g., store customer details once, even if they place many orders. |
| Maintain Data Integrity| Easier to ensure accurate data when split logically.                        |
| Easy Updates           | Update a customer's address in one place, not everywhere.                  |
| Better Organization    | Tables represent real-world entities (e.g., Customers, Orders, Products).   |
| Faster Queries         | Smaller, normalized tables allow faster filtering and joins.                |


# 🔗 What is a JOIN in MySQL?
A JOIN is used to combine rows from two or more tables based on a related column between them (usually a foreign key).
```sql
SELECT columns
FROM table1
JOIN table2
ON table1.common_field = table2.common_field;
```
# 💡 Types of Joins in MySQL
## 1. INNER JOIN
- Returns only matching rows from both tables.

```sql
SELECT employees.name, departments.name
FROM employees
INNER JOIN departments
ON employees.dept_id = departments.id;
```
- ✅ Use when: You only want data where there's a match in both tables.

## 2. LEFT JOIN (LEFT OUTER JOIN)
- Returns all rows from the left table, and matched rows from the right.
- If no match, NULLs are returned.
```sql
SELECT customers.name, orders.id
FROM customers
LEFT JOIN orders
ON customers.id = orders.customer_id;
```
- ✅ Use when: You want all customers, even if they haven’t placed any orders.

## 3. RIGHT JOIN (RIGHT OUTER JOIN)
Returns all rows from the right table, and matched rows from the left.

```sql
SELECT orders.id, customers.name
FROM orders
RIGHT JOIN customers
ON orders.customer_id = customers.id;
```
- ✅ Use when: You want all orders, even if customer info is missing.

## 4. FULL JOIN (Not in MySQL directly)
MySQL doesn't support FULL OUTER JOIN directly. You can simulate it using UNION:

```sql
SELECT * FROM A LEFT JOIN B ON A.id = B.id
UNION
SELECT * FROM A RIGHT JOIN B ON A.id = B.id;
```

## 5. CROSS JOIN
Returns all possible combinations (Cartesian product).
```sql
SELECT * FROM shirts CROSS JOIN pants;
```
- ✅ Use when: You want combinations (e.g., every shirt with every pant).

