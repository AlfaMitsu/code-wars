SQL Basics: Simple Hierarchical structure

    WITH RECURSIVE employee_levels AS (
        -- Base case: Employees with no manager (level 1)
        SELECT 
            1 AS level,
            e.id,
            e.first_name,
            e.last_name,
            e.manager_id
        FROM employees e
        WHERE e.manager_id IS NULL
    
        UNION ALL
    
        -- Recursive case: Employees with a manager
        SELECT 
            el.level + 1 AS level,
            e.id,
            e.first_name,
            e.last_name,
            e.manager_id
        FROM employees e
        INNER JOIN employee_levels el ON e.manager_id = el.id
    )
    SELECT 
        level,
        id,
        first_name,
        last_name,
        manager_id
    FROM employee_levels
    ORDER BY level, id;
