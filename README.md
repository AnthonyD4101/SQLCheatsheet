# SQLCheatsheet

SQL practice examples, tips and resources.

[Basic SQL Course Reference from 'LearnSQL'](https://learnsql.com/dashboard/)

## Basic Syntax

```SQL
SELECT columnName1, columnName2, ...
FROM tableName;
```

- The `SELECT` clause allows you to specify what data you want returned
- The `FROM` clause chooses from what table you'll be pulling data from<br>
  <br>

```SQL
SELECT columnName1, columnName2, ...
FROM tableName
WHERE givenCondition;
```

- With the `WHERE` clause, you can extract/filter certain records that fulfill a specified condition<br>
  <br>

## Conditional Operators

Here are some conditional operators that can be used in SQL:

- =
- != or <>
- \> , <, >=, <=
- `AND`
- `OR`
- `NOT`
- `IS NULL` or `IS NOT NULL`
- `LIKE` or `NOT LIKE`
- `IN` or `NOT IN`
- `BETWEEN` or `NOT BETWEEN`
- `EXISTS`

## Aggregate Functions & Grouping

Functions that performs a calculation on a set of values, and returns a single value.

- Often used with the `GROUP BY` clause

```sql
MIN() - returns the smallest value within the selected column
MAX() - returns the largest value within the selected column
COUNT() - returns the number of rows in a set
SUM() - returns the total sum of a numerical column
AVG() - returns the average value of a numerical column
```

## Wildcard Operators

Percent Sign (%): Represents zero, one, or multiple characters.

```sql
-- Finds any values that start with 'a'
SELECT * FROM employees WHERE name LIKE 'a%';

-- Finds any values that end with 'a'
SELECT * FROM employees WHERE name LIKE '%a';

-- Finds any values that contain 'a'
SELECT * FROM employees WHERE name LIKE '%a%';
```

Underscore (\_): Represents a single character.

```sql
-- Finds any values that have 'a' as the first character and any character as the second
SELECT * FROM employees WHERE name LIKE 'a_';

-- Finds any values that have 'a' as the second character
SELECT * FROM employees WHERE name LIKE '_a_';

-- Finds any values that have exactly three characters, with 'a' as the second character
SELECT * FROM employees WHERE name LIKE '_a_';
```

Combining % and \_

```sql
-- Finds any values that start with 'a', followed by any single character, and end with 'n'
SELECT * FROM employees WHERE name LIKE 'a_n%';

-- Finds any values where 'a' is the first character, followed by any two characters, and ending with 'n'
SELECT * FROM employees WHERE name LIKE 'a__n%';
```

## `JOIN` Clauses
