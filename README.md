# Exercise 2 – Student Database

## Description
In this exercise, we create a database with a table called `student`. The table stores information about students, including their ID, first name, last name, and comments.

## 1. Create the Database

```sql
CREATE DATABASE studenter;
USE studenter;
```

## 2. Create the Student Table

```sql
CREATE TABLE student (
    sid INT NOT NULL PRIMARY KEY,
    fname VARCHAR(20) NOT NULL,
    lname VARCHAR(20) NOT NULL,
    comment TEXT NULL
);
```

### Table Structure

| Column | Data Type | Allows NULL | Key |
|--------|-----------|-------------|-----|
| sid | INT | No | PRIMARY KEY |
| fname | VARCHAR(20) | No | No |
| lname | VARCHAR(20) | No | No |
| comment | TEXT | Yes | No |

## 3. Insert at Least 3 Students

```sql
INSERT INTO student (sid, fname, lname, comment)
VALUES
(1, 'Ali', 'Ahmed', 'Good student'),
(2, 'Sara', 'Karlsson', 'Enjoys programming'),
(3, 'Erik', 'Svensson', NULL);
```

## 4. Display All Students

```sql
SELECT * FROM student;
```

## 5. Expected Result

| sid | fname | lname | comment |
|-----|-------|-------|---------|
| 1 | Ali | Ahmed | Good student |
| 2 | Sara | Karlsson | Enjoys programming |
| 3 | Erik | Svensson | NULL |

## 6. Explanation

- **sid:** The student's unique ID and the primary key of the table.
- **fname:** The student's first name, with a maximum of 20 characters.
- **lname:** The student's last name, with a maximum of 20 characters.
- **comment:** An optional comment about the student.
- **PRIMARY KEY:** Ensures that each student has a unique ID.
- **NOT NULL:** Means that the column must contain a value.
- **NULL:** Means that a value can be missing.

## Conclusion

In this exercise, we have:
- Created a database named `studenter`.
- Created a table named `student`.
- Defined a primary key and required fields.
- Inserted three students into the table.
- Retrieved all students using the `SELECT` statement.
