Best-Selling Books (SQL for Beginners #5)

    SELECT
        name,
        author,
        copies_sold
    FROM
        books
    ORDER BY
        copies_sold DESC
    LIMIT 5;
