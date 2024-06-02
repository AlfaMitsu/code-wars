On the Canadian Border (SQL for Beginners #2)

    SELECT name, country
    FROM travelers
    WHERE country NOT IN ('Canada', 'Mexico', 'USA');
