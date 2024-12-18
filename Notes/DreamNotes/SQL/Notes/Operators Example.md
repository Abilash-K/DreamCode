
## Data Types

### Numeric Types
- **INT**: Stores integer values. Suitable for whole numbers.
- **SMALLINT**: Smaller range of integer values.
- **BIGINT**: Large range of integer values.
- **DECIMAL(p, s)** / **NUMERIC(p, s)**: Fixed-point numbers. `p` defines precision (total digits), `s` defines scale (digits after decimal).
- **FLOAT** / **REAL**: Approximate numeric values for floating-point operations.

### Character/String Types
- **CHAR(n)**: Fixed-length character string. Pads with spaces if input is shorter.
- **VARCHAR(n)**: Variable-length character string with a defined maximum length.
- **TEXT**: Stores large strings of text without a specific length limit.

### Date and Time Types
- **DATE**: Stores date values (e.g., `YYYY-MM-DD`).
- **TIME**: Stores time values (e.g., `HH:MM:SS`). Can include timezone information.
- **TIMESTAMP**: Combines date and time values (e.g., `YYYY-MM-DD HH:MM:SS`). Can include timezone information.
- **INTERVAL**: Represents a duration of time (e.g., `1 year 2 months`).

### Boolean
- **BOOLEAN**: Stores `TRUE`, `FALSE`, or `NULL`.

### Other Types
- **UUID**: Stores a universally unique identifier.
- **ARRAY**: Stores arrays of values (e.g., `{1,2,3}`).
- **JSON** / **JSONB**: Stores JSON data. `JSONB` is a binary format optimized for indexing and querying.
- **XML**: Stores XML data.

---

## Operators

### Arithmetic Operators
- **`+`**: Addition of two numbers.
- **`-`**: Subtraction of two numbers.
- **`*`**: Multiplication of two numbers.
- **`/`**: Division of two numbers.
- **`%`**: Modulo operation (remainder of division).

### Comparison Operators
- **`=`**: Checks if two values are equal.
- **`!=`** or **`<>`**: Checks if two values are not equal.
- **`>`**: Checks if the left value is greater than the right value.
- **`<`**: Checks if the left value is less than the right value.
- **`>=`**: Checks if the left value is greater than or equal to the right value.
- **`<=`**: Checks if the left value is less than or equal to the right value.

### Logical Operators
- **`AND`**: Combines two conditions. Both must be true.
- **`OR`**: Combines two conditions. At least one must be true.
- **`NOT`**: Negates a condition.

### Other Operators
- **`BETWEEN ... AND ...`**: Checks if a value is within a range.
- **`IN (...)`**: Checks if a value matches any value in a list.
- **`LIKE`**: Pattern matching using `%` (any number of characters) or `_` (single character).
- **`IS NULL`**: Checks if a value is `NULL`.
- **`IS NOT NULL`**: Checks if a value is not `NULL`.
- **`EXISTS`**: Checks if a subquery returns any rows.

