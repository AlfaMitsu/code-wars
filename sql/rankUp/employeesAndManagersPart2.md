Employees and managers: part 2

    WITH RECURSIVE ManagerHierarchy AS (
        SELECT id, name, manager_id, CAST('' AS TEXT) AS management_chain
        FROM employees
        WHERE manager_id IS NULL
        UNION ALL
        SELECT e.id, e.name, e.manager_id,
               CONCAT(ManagerHierarchy.management_chain, 
                      CASE WHEN ManagerHierarchy.management_chain = '' THEN '' ELSE ' -> ' END,
                      ManagerHierarchy.name, ' (', ManagerHierarchy.id, ')') AS management_chain
        FROM employees e
        JOIN ManagerHierarchy ON e.manager_id = ManagerHierarchy.id
    )
    SELECT id, name, management_chain
    FROM ManagerHierarchy
    ORDER BY id;
