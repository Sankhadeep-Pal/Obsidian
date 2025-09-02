# a
## a
### a
[[version control system]]
*df*
***fdffadsfdsfsdnoiudsngnvdonfviodsnvonv***
**dfdsvijndisnvo**
- dvjsvj
+ ddpsfkmds
_vkomdofpmv_
__fkdsmpovmpdmv__
___dsmvpomdposmvpo___
1) kvpmfvk
2. gkgmvp
~~kovmm~~
dsf^gyvydcvvf
<b><u>dfidjnfindonfdv</u></b>
<h1>fdmfiopmdomf</h1>
==odvos==
`cmdsmcm`
$fmvodmvmbo$
%% blm'fmbmlfm %%
- [ ] vkm;vmfv
- [ ]
> vl'dmfmmvbm

| dlc,dd | dlkdlc |     |
| ------ | ------ | --- |
| vdlm   | dlp,c  |     |
|        |        |     |

> [!NOTE] Title
> Contents

```
movmovmovm[v]
```
$$
ffvgpoofmvmomv
$$
[omvfomov](https://youtu.be/xvFZjo5PgG0)

---

> [!NOTE]
> [^2]: lvldmsmdsm

yWxxnbecwBEQpee3IoX74cwoSvsrjixaP1HA5qeC



## Tables
In **MySQL**, a **table** is the **fundamental structure where data is stored**. You can think of it like a spreadsheet: it has **rows** and **columns**, where each row represents a single record, and each column represents a field or attribute of that record.

### Structure of a Table

- **Columns (Fields)**: Define the type of data stored, e.g., `id`, `name`, `email`.

- **Rows (Records)**: Each row stores a single instance of data.

- **Example Table: `users`**
	
|id|name|email|age|
|---|---|---|---|
|1|Sankho| sankho@mail.com |21|
|2|Riya| riya@mail.com |22|
	
- Here, `id`, `name`, `email`, `age` are **columns**.
	
- Each row is a **record**.

---

## **3. Describe a Table**

View structure (columns, types, keys, constraints).

```sql
DESCRIBE users;
```

---

## **4. Alter a Table**

Modify the structure after creation.

- **Add a column:**
    

```sql
ALTER TABLE users ADD COLUMN phone VARCHAR(15);
```

- **Modify a column type:**
    

```sql
ALTER TABLE users MODIFY COLUMN age SMALLINT;
```

- **Rename a column:**
    

```sql
ALTER TABLE users CHANGE COLUMN phone mobile VARCHAR(20);
```

- **Drop a column:**
    

```sql
ALTER TABLE users DROP COLUMN age;
```

---

## **5. Rename a Table**

```sql
RENAME TABLE users TO customers;
```

---

## **6. Drop a Table**

Permanently delete a table and its data.

```sql
DROP TABLE users;
```

⚠️ **Warning**: This cannot be undone unless you have a backup.

---

## **7. Truncate a Table**

Delete all rows but keep the structure.

```sql
TRUNCATE TABLE users;
```

---

✅ **Summary**:

- `CREATE TABLE` → build a new table
    
- `SHOW/DESCRIBE` → inspect tables
    
- `ALTER` → modify structure
    
- `RENAME` → change table name
    
- `DROP` → delete table
    
- `TRUNCATE` → clear all data but keep structure
    

---

Do you want me to also cover **advanced table queries like indexing, foreign keys, and joins** (how tables connect with each other)? That’s where relational databases really shine.



---

#### Aggregate Functions

Aggregate functions perform calculations on a set of rows and return **a single value**.  
They’re often used with `GROUP BY` to group rows before applying the function.

**🔑 Common Aggregate Functions**

##### 1. COUNT ()

- Returns the number of rows (non-NULL values if a column is specified).
    
```mysql
SELECT COUNT(*) AS total_students
FROM students;

SELECT COUNT(age) AS known_ages
FROM students;
```

##### 2. SUM ()

- Returns the total sum of a numeric column.
    
```mysql
SELECT SUM(salary) AS total_salary
FROM employees;
```

##### 3. AVG ()

- Returns the average value of a numeric column.
    
```mysql
SELECT AVG(marks) AS avg_marks
FROM students;
```

##### 4. MIN ()

- Returns the smallest value in a column.
    
```mysql
SELECT MIN(price) AS cheapest_item
FROM products;
```

##### 5. MAX ()

- Returns the largest value in a column.
    
```mysql
SELECT MAX(price) AS most_expensive
FROM products;
```

##### 6. GROUP_CONCAT () (MySQL-specific)

- Concatenates values from a group into a single string.
    
```sql
SELECT department, GROUP_CONCAT(name) AS employees
FROM staff
GROUP BY department;
```

##### ⚡ Usage with GROUP BY
Aggregate functions are often paired with `GROUP BY` to calculate values per group.

```sql
SELECT department, COUNT(*) AS total_emp, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;
```

##### ⚠️ Key Points to Remember

- `WHERE` filters rows **before** aggregation.

- `HAVING` filters rows **after** aggregation.

```sql
-- Only show departments with more than 5 employees
SELECT department, COUNT(*) 
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
[[#**4. LIKE**]]```

- Aggregate functions **ignore NULL values** (except `COUNT(*)`, which counts all rows).

---

### Updating into the Table
The `UPDATE` statement is used to modify existing records (rows) in a table.

#### 🔑 Syntax

```mysql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
[WHERE condition]
[LIMIT n];
```

- **UPDATE table_name** → The table to be updated.

- **SET** → Defines which columns to update and their new values.

- **WHERE** (optional but important!) → Specifies which rows should be updated. Without `WHERE`, **all rows** in the table will be updated.

- **LIMIT** (optional) → Restricts how many rows get updated (useful for testing or safety).

#### ✅ Update table Example

```Mysql
# Update Command: to update in existing rows
UPDATE userInfo
SET follow = 150
WHERE age = 15;
SELECT * FROM userInfo;

# Teacher said that if we run update command form the first time then there will be error & we have to run 
# SET SQL_SAFE_UPDATE = 0; but, I guess I don't need it beacuse i am in linux.
```

---

### Deleting Data from Table
The `DELETE` statement is used to **remove existing rows** from a table.

#### 🔑 Syntax

```sql
DELETE FROM table_name
[WHERE condition]
[LIMIT n];
```

- **DELETE FROM table_name** → Specifies the table from which rows will be deleted.

- **WHERE** (optional but critical) → Defines which rows to delete. Without `WHERE`, **all rows** are deleted.

- **LIMIT** (optional) → Restricts the number of rows deleted (useful for large datasets or testing).

#### ✅ Example

```Mysql
# Delete Command: to delete existing rows
DELETE FROM posts 
WHERE id = 102;
SELECT * FROM posts;

# Disclaimer: If we don't any type of condition then it will delete all rows... Be careful.
```

---
