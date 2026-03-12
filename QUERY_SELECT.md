1. Selezionare tutti gli studenti nati nel 1990 (160)

```sql
SELECT *
FROM db_university.students
WHERE YEAR(date_of_birth) = 1990;
```

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

```sql
    SELECT *
    FROM db_university.courses
    WHERE courses.cfu > 10
```

3. Selezionare tutti gli studenti che hanno più di 30 anni

```sql
SELECT *, TIMESTAMPDIFF(YEAR, students.date_of_birth, CURDATE()) AS "age"
FROM db_university.students
WHERE TIMESTAMPDIFF(YEAR, students.date_of_birth, CURDATE()) > 30
```

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
   laurea (286)

```sql
SELECT *
FROM db_university.courses
WHERE period LIKE "I semestre" AND year LIKE 1
```

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
   20/06/2020 (21)

```sql
SELECT *
FROM db_university.exams
WHERE date LIKE "2020-06-20" AND hour > "14:00:00"
```

6. Selezionare tutti i corsi di laurea magistrale (38)
7. Da quanti dipartimenti è composta l'università? (12)
8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
