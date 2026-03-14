1. Contare quanti iscritti ci sono stati ogni anno

```sql
SELECT YEAR(enrolment_date) AS year, COUNT() AS students
FROM db_university.students
GROUP BY year
ORDER BY year
```

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```sql
SELECT office_address, COUNT(office_address) AS teachers_offices
FROM db_university.teachers
GROUP BY office_address
ORDER BY teachers_offices DESC
```

3. Calcolare la media dei voti di ogni appello d'esame

```sql
SELECT exam_id, AVG(vote) AS average_vote
FROM db_university.exam_student
GROUP BY exam_id
```

4. Contare quanti corsi di laurea ci sono per ogni dipartimento

```sql
SELECT department_id, COUNT(name) AS number_of_courses
FROM db_university.degrees
GROUP BY department_id
```
