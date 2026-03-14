1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

```sql
SELECT
degrees.id,
degrees.name,
students.name,
students.surname
FROM db_university.degrees
INNER JOIN db_university.students
ON degrees.id = students.degree_id
WHERE degrees.name = "Corso di Laurea in Economia"
```

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
   Neuroscienze

```sql
SELECT department_id, degrees.name, degrees.level
FROM db_university.degrees
INNER JOIN db_university.departments ON department_id
WHERE degrees.level = "magistrale" AND departments.name = "Dipartimento di Neuroscienze"
```

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

```sql
SELECT teachers.id AS teacher_id, teachers.name, teachers.surname, courses.name AS course_name
FROM db_university.teachers
INNER JOIN course_teacher ON teacher_id = id
INNER JOIN courses ON course_id = courses.id
WHERE teachers.id = 44
```

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
   sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
   nome

```sql
SELECT students.id AS student_id, students.surname, students.name, degrees.name, degrees.level, departments.name
FROM db_university.students
INNER JOIN degrees ON degree_id = degrees.id
INNER JOIN departments ON department_id = departments.id
ORDER BY students.surname, students.name ASC
```

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

```sql
SELECT degrees.id AS degrees_id, degrees.name AS degrees_name, courses.name AS course_name, teachers.name AS teacher_name, teachers.surname AS teacher_surname
FROM db_university.degrees
INNER JOIN courses ON degree_id = degrees.id
INNER JOIN course_teacher ON course_teacher.course_id = courses.id
INNER JOIN teachers ON course_teacher.teacher_id = teachers.id
ORDER BY degrees_id
```

6. Selezionare tutti i docenti che insegnano nel Dipartimento di
   Matematica (54)

```sql
SELECT teachers.id AS teacher_id, departments.name, teachers.name AS teacher_name, teachers.surname AS teacher_surname
FROM db_university.teachers
INNER JOIN course_teacher ON course_teacher.teacher_id = teachers.id
INNER JOIN courses ON course_teacher.course_id = courses.id
INNER JOIN degrees ON courses.degree_id = degrees.id
INNER JOIN departments ON degrees.department_id = departments.id
WHERE departments.name = "Dipartimento di Matematica"
GROUP BY teachers.id, departments.name, teachers.name, teachers.surname
ORDER BY teachers.id ASC
```

7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
   per ogni esame, stampando anche il voto massimo. Successivamente,
   filtrare i tentativi con voto minimo 18.

```sql

```
