# SQL Data Types Notes with Examples

SQL data types define the kind of data a column can store. They are grouped into categories like numeric, string, date/time, binary, and boolean.

---

## 1. Numeric Data Types

| Data Type      | Description                            | Example Value     | Example Use Case                          |
|----------------|----------------------------------------|-------------------|-------------------------------------------|
| `INT`          | Integer, whole numbers                 | `25`              | `age INT`                                 |
| `SMALLINT`     | Smaller range of integers              | `32000`           | `stock_quantity SMALLINT`                 |
| `BIGINT`       | Larger range of integers               | `9223372036854775807` | `views BIGINT`                      |
| `DECIMAL(p,s)` | Fixed-point number (precision, scale)  | `12345.67`        | `price DECIMAL(10,2)`                     |
| `NUMERIC(p,s)` | Same as DECIMAL                        | `9999.99`         | `salary NUMERIC(8,2)`                     |
| `FLOAT`        | Approximate floating-point number      | `3.14`            | `temperature FLOAT`                       |
| `DOUBLE`       | Double precision floating-point        | `3.1415926535`    | `latitude DOUBLE`                         |

---

## 2. String (Character) Data Types

| Data Type       | Description                             | Example Value        | Example Use Case              |
|------------------|-----------------------------------------|----------------------|-------------------------------|
| `CHAR(n)`        | Fixed-length string (padded with spaces)| `'Y'`, `'AB   '`     | `gender CHAR(1)`              |
| `VARCHAR(n)`     | Variable-length string (max n chars)    | `'John Doe'`         | `name VARCHAR(100)`           |
| `TEXT`           | Large text data                         | `'This is a long blog post...'` | `description TEXT`      |
| `ENUM`           | One value from a predefined list        | `'small'`            | `size ENUM('small','medium','large')` |

---

## 3. Date and Time Data Types

| Data Type     | Description                    | Example Value             | Example Use Case             |
|----------------|--------------------------------|----------------------------|------------------------------|
| `DATE`         | Date only                      | `'2025-07-17'`             | `birth_date DATE`            |
| `TIME`         | Time only                      | `'14:30:00'`               | `start_time TIME`            |
| `DATETIME`     | Date and time                  | `'2025-07-17 14:30:00'`    | `created_at DATETIME`        |
| `TIMESTAMP`    | Date and time with time zone awareness | `'2025-07-17 14:30:00'` | `updated_at TIMESTAMP`       |
| `YEAR`         | Year only                      | `'2025'`                   | `graduation_year YEAR`       |

---

## 4. Binary Data Types

| Data Type     | Description                        | Example Value           | Example Use Case              |
|---------------|------------------------------------|-------------------------|-------------------------------|
| `BINARY(n)`   | Fixed-length binary data           | `0x4D7953514C`          | `hash BINARY(10)`             |
| `VARBINARY(n)`| Variable-length binary data        | `0xFFD8FFE000104A4649`  | `file_data VARBINARY(255)`    |
| `BLOB`        | Binary Large Object (up to 4GB)    | (image file bytes)      | `profile_picture BLOB`        |

---

## 5. Boolean Type

| Data Type  | Description                  | Example Value | Example Use Case        |
|------------|------------------------------|----------------|-------------------------|
| `BOOLEAN`  | Stores TRUE or FALSE         | `TRUE`, `FALSE`| `is_active BOOLEAN`     |

_Note: In MySQL, `BOOLEAN` is treated as a synonym for `TINYINT(1)`._

---

## Additional Notes

- Use `DECIMAL` or `NUMERIC` for **financial data** to maintain accuracy.
- `TEXT` and `BLOB` types **cannot** have default values.
- `VARCHAR` is more efficient than `CHAR` for variable-length data.
- `TIMESTAMP` often has default value as `CURRENT_TIMESTAMP` and is ideal for **auto-tracking last modified time**.

