## Aggregate Functions

Aggregate functions perform calculations on a set of rows and return a single result.

### Common Aggregate Functions

- **`COUNT()`**: Returns the number of rows.
  - Example: `SELECT COUNT(*) FROM employees;`

- **`SUM()`**: Returns the total sum of a numeric column.
  - Example: `SELECT SUM(salary) FROM employees;`

- **`AVG()`**: Returns the average value of a numeric column.
  - Example: `SELECT AVG(salary) FROM employees;`

- **`MAX()`**: Returns the maximum value in a column.
  - Example: `SELECT MAX(salary) FROM employees;`

- **`MIN()`**: Returns the minimum value in a column.
  - Example: `SELECT MIN(salary) FROM employees;`

### Using Aggregate Functions with `GROUP BY`
- Aggregate functions are often used with the `GROUP BY` clause to group rows sharing a property and perform calculations on each group.
  - Example: `SELECT department, AVG(salary) FROM employees GROUP BY department;`

### Using Aggregate Functions with `HAVING`
- The `HAVING` clause filters groups based on conditions.
  - Example: `SELECT department, COUNT(*) FROM employees GROUP BY department HAVING COUNT(*) > 10;`

