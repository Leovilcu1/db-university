1. Contare quanti iscritti ci sono stati ogni anno

    SELECT COUNT(`id`) AS `iscritti` ,YEAR(`date_of_birth`) AS `anno`
    FROM `students`
    GROUP BY `anno`;

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

    SELECT COUNT(`id`) AS `nr_Insegnanti`,`office_address`
    FROM `teachers`
    GROUP BY `office_address`;
    
3. Calcolare la media dei voti di ogni appello d'esame

    SELECT AVG(`vote`) AS `voto_medio`,`exam_id`
    FROM `exam_student`
    GROUP BY`exam_id`;

4. Contare quanti corsi di laurea ci sono per ogni dipartimento

    SELECT COUNT(`id`) AS `nr_corsi`, `department_id`
    FROM `degrees`
    GROUP BY `department_id`;   