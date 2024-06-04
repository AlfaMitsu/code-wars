Books That Are Always Being Returned

    SELECT b.book_id, b.title
    FROM books b
    JOIN loans l ON b.book_id = l.book_id
    GROUP BY b.book_id, b.title
    HAVING COUNT(*) = COUNT(l.return_date)
    ORDER BY b.book_id DESC;
