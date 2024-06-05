Youngest Team Mmembers

    WITH RankedEmployees AS (
        SELECT
            employee_id,
            full_name,
            team,
            birth_date,
            ROW_NUMBER() OVER (PARTITION BY team ORDER BY birth_date DESC) AS rnk
        FROM employees
    )
    SELECT
        employee_id,
        full_name,
        team,
        birth_date
    FROM RankedEmployees
    WHERE rnk = 1
    ORDER BY team;
