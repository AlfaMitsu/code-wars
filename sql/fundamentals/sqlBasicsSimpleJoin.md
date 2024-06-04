SQL Basics: Simple JOIN

    SELECT
        p.*,
        c.name AS company_name
    FROM
        products p
    JOIN
        companies c ON p.company_id = c.id;
