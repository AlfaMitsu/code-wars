Enumerate consecutive runs

    WITH run_identification AS (
        SELECT
            id,
            value,
            CASE
                WHEN value = LAG(value) OVER (ORDER BY id) AND id = LAG(id) OVER (ORDER BY id) + 1 THEN 0
                ELSE 1
            END AS new_run
        FROM entries
    ),
    run_enumeration AS (
        SELECT
            id,
            value,
            SUM(new_run) OVER (ORDER BY id) AS run_id
        FROM run_identification
    )
    SELECT
        id,
        value,
        run_id
    FROM run_enumeration
    ORDER BY id;
