SQL with LOTR: Elven Wildcards

    SELECT 
      CONCAT(UPPER(LEFT(firstname, 1)), SUBSTRING(firstname, 2), ' ', UPPER(LEFT(lastname, 1)), SUBSTRING(lastname, 2)) AS shortlist
    FROM 
      Elves
    WHERE 
      firstname LIKE '%tegil%' OR
      lastname LIKE '%astar%';
