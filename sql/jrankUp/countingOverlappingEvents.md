Counting Overlapping Events

    WITH combined_times AS (
        SELECT entry_time AS time, 1 AS change
        FROM visits
        UNION ALL
        SELECT exit_time AS time, -1 AS change
        FROM visits
    ),
    running_counts AS (
        SELECT time,
               SUM(change) OVER (ORDER BY time) AS current_count
        FROM combined_times
    ),
    max_counts AS (
        SELECT MAX(current_count) AS max_count
        FROM running_counts
    )
    SELECT time AS when_happened, current_count AS visits_count
    FROM running_counts
    WHERE current_count = (SELECT max_count FROM max_counts)
    ORDER BY time
    LIMIT 1;
