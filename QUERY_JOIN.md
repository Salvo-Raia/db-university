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
