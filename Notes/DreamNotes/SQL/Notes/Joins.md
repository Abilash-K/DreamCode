
Joins are used to combine rows from two or more tables based on a related column between them.

### Types of Joins

A **plain JOIN** is essentially shorthand for an **INNER JOIN**, as many database systems treat `JOIN` without a qualifier (like LEFT, RIGHT, or FULL) as the same as `INNER JOIN`. Here's how it fits into the notes:

---

### Plain JOIN

- Equivalent to `INNER JOIN`. It only returns rows where there is a match in both tables.
- Commonly used for simplicity when there’s no ambiguity about the type of join.

**Syntax:**

```sql
SELECT columns
FROM table1
JOIN table2
ON table1.column = table2.column;
```

**Example:**

```sql
SELECT employees.name, departments.department_name
FROM employees
JOIN departments
ON employees.department_id = departments.id;
```

**Key Points:**

- Use `JOIN` for simplicity, especially when the intention is clear.
- Some databases explicitly require `INNER` to avoid confusion.

---

#### 1. INNER JOIN
- Returns only the rows where there is a match in both tables.
- If no match is found, the row is excluded from the result.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```
**Example:**
```sql
SELECT employees.name, departments.department_name
FROM employees
INNER JOIN departments
ON employees.department_id = departments.id;
```

#### 2. LEFT JOIN (or LEFT OUTER JOIN)
- Returns all rows from the left table, and the matched rows from the right table.
- If no match is found, NULL is returned for the right table's columns.

**Syntax:**
```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```
**Example:**
```sql
SELECT employees.name, departments.department_name
FROM employees
LEFT JOIN departments
ON employees.department_id = departments.id;
```

#### 3. RIGHT JOIN (or RIGHT OUTER JOIN)
- Returns all rows from the right table, and the matched rows from the left table.
- If no match is found, NULL is returned for the left table's columns.

**Syntax:**
```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```
**Example:**
```sql
SELECT employees.name, departments.department_name
FROM employees
RIGHT JOIN departments
ON employees.department_id = departments.id;
```

#### 4. FULL JOIN (or FULL OUTER JOIN)
- Returns all rows when there is a match in either table.
- Rows without matches in one table will have NULLs for the columns of the other table.

**Syntax:**
```sql
SELECT columns
FROM table1
FULL JOIN table2
ON table1.column = table2.column;
```
**Example:**
```sql
SELECT employees.name, departments.department_name
FROM employees
FULL JOIN departments
ON employees.department_id = departments.id;
```

#### 5. CROSS JOIN
- Produces a Cartesian product of the two tables.
- Every row from the first table is paired with every row from the second table.

**Syntax:**
```sql
SELECT columns
FROM table1
CROSS JOIN table2;
```
**Example:**
```sql
SELECT employees.name, projects.project_name
FROM employees
CROSS JOIN projects;
```

### Self Join
- A self join is when a table is joined with itself.
- Useful for hierarchical or comparison-based queries.

**Syntax:**
```sql
SELECT a.column, b.column
FROM table a
INNER JOIN table b
ON a.common_column = b.common_column;
```
**Example:**
```sql
SELECT e1.name AS Employee, e2.name AS Manager
FROM employees e1
INNER JOIN employees e2
ON e1.manager_id = e2.id;
```

### Joining More Than Two Tables

- You can join multiple tables by chaining multiple join clauses together.
- Each join must have its own `ON` clause specifying the relationship between the tables.

**Syntax:**

```sql
SELECT columns
FROM table1
INNER JOIN table2 ON table1.column = table2.column
INNER JOIN table3 ON table2.column = table3.column;
```

**Example:**

```sql
SELECT employees.name, departments.department_name, locations.city
FROM employees
INNER JOIN departments ON employees.department_id = departments.id
INNER JOIN locations ON departments.location_id = locations.id;
```


### Key Points
- Use **aliases** (like `a` and `b` in the self join) for better readability.
- Ensure join conditions are properly defined to avoid Cartesian products unless intended.
- Use **indexes** on join columns to optimize performance.

