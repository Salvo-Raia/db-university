![Boolean Tech Academy](https://img.shields.io/badge/Boolean_Tech_Academy-001632?style=for-the-badge)

# 🎓 Exercise 47/50 - University Database

Design and implement a relational database for a university, then practice SQL queries to retrieve and analyze its data.

## 📌 Project Overview

| Property | Details |
|:--|:--|
| Repository | `db-university` |
| Category | Boolean Tech Academy |
| Type | Exercise |
| Exercise | 47/50 |

## 🎯 Assignment

Create a relational database to manage the information and relationships within a university.

### Part 1 - Database Design

Identify the entities, define their attributes and data types, and establish the relationships between the tables.

The database must represent the following entities and relationships:

- **Departments:** Each department offers multiple degree programs.
- **Degree Programs:** Each degree program belongs to a department and includes multiple study courses.
- **Study Courses:** Each study course belongs to a degree program and can be taught by multiple teachers.
- **Teachers:** Teachers can be assigned to multiple study courses.
- **Exam Sessions:** Each study course can have multiple exam sessions.
- **Students:** Each student is enrolled in only one degree program.
- **Exam Registrations:** Students can register for multiple exam sessions.
- **Exam Results:** For every exam session attended by a student, the database must store the grade obtained, including failing grades.

#### Departments

Create a table with the following fields:

- `id`
- `name`
- `number_of_courses`
- `code`
- `description`
- `headquarters_address`
- `secretariat_email`
- `secretariat_phone`

#### Degree Programs

Create a table with the following fields:

- `id`
- `name`
- `code`
- `number_of_study_courses`
- `duration`
- `degree_level` (Bachelor's, Master's, PhD)
- `credits`
- `coordinator`
- `description`

#### Study Courses

Create a table with the following fields:

- `id`
- `name`
- `code`
- `credits`
- `semester`
- `professors`
- `total_hours`
- `description`
- `degree_program_id`

Define the appropriate tables, columns, data types, primary keys, foreign keys, and relationships to represent the complete university structure.

#### Database Diagram

Use [draw.io](https://www.drawio.com/) to create the entity-relationship diagram.

Once completed:

- Export the diagram as a JPG image.
- Upload the exported image to the repository.

### Part 2 - Database Schema and SQL Queries

- Create a new database using MySQL Workbench.
- Import the provided database schema.
- Execute the SQL queries included in the assignment attachments.
- Test the queries using MySQL Workbench.
- Save the solutions in a Markdown file and upload it to the repository.

### Part 3 - GROUP BY Queries

Using the same university database, execute the additional queries provided in the assignment.

- Test the queries using MySQL Workbench.
- Save the solutions in a separate Markdown file.
- Upload the file to the `db-university` repository.

### Part 4 - JOIN Queries

Continue working with the same database and execute the provided JOIN queries.

- Test the queries using MySQL Workbench.
- Save the solutions in a separate Markdown file.
- Upload the file to the `db-university` repository.

## 🛠️ Technologies

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![MySQL Workbench](https://img.shields.io/badge/MySQL_Workbench-4479A1?style=flat-square&logo=mysql&logoColor=white)

## 💡 What I Learned

- Designing relational database schemas.
- Identifying entities, attributes, and relationships.
- Defining primary keys and foreign keys.
- Modeling one-to-many and many-to-many relationships.
- Managing database structures with MySQL Workbench.
- Writing and executing SQL queries.
- Grouping and aggregating data with `GROUP BY`.
- Retrieving related data using `JOIN`.
- Documenting database structures and SQL solutions.

## ©️ Credits

Exercise assigned by **Boolean Tech Academy** as part of the Web Development course - Class 152 - Year 2025-2026


