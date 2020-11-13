---
author: kapnobatai136

type: normal

category: must-know

tags:
  - insert
  - syntax

---

# Order Matters II

---

## Content

The order also matters when we insert values into specific columns.

Take this table of `employees` for example:

| id | name | position  | age |
|----|------|-----------|-----|
| 1  | Will | Developer | 29  |

If we tried this `INSERT` command:

```sql
INSERT INTO employees VALUES
(2, "Mathilda", 31, "Project Manager");
```

We would get:

| id | name     | position  | age             |
|----|----------|-----------|-----------------|
| 1  | Will     | Developer | 29              |
| 2  | Mathilda | 31        | Project Manager |

The same applies to inserting into specific columns:

```sql
INSERT INTO employees
(position, name, age)
VALUES
("Senior Developer", 23, "Bill");
```

This is how the table will look like:

| id   | name     | position         | age             |
|------|----------|------------------|-----------------|
| 1    | Will     | Developer        | 29              |
| 2    | Mathilda | 31               | Project Manager |
| NULL | 23       | Senior Developer | Bill            |

> 💡 You should make sure you are inserting values in the correct order. Depending on the RDBMS used, the commands above could also throw an error.

---

## Practice

What will the table look like after running the following `INSERT` command?

```sql
INSERT INTO students VALUES
(4, 8.7, "Comp Sci", "Adam");
```

| id  | name   | major    | final_grade |
|-----|--------|----------|-------------|
| 1   | Chris  | Arts     | 9.3         |
| 2   | Rachel | Mech Eng | 8.3         |
| ??? | ???    | ???      | ???         |

- 4
- 8.7
- Comp Sci
- Adam
- 3

---

## Revision

Complete the command to insert the values **in the correct order**.

| name     | country        | country_iso_code |
|----------|----------------|------------------|
| London   | United Kingdom | GBR              |
| New York | United States  | USA              |

```sql
INSERT INTO cities
(country_iso_code, name, country)
VALUES
(???, ???, ???);
```

- "FRA"
- "Paris"
- "France"