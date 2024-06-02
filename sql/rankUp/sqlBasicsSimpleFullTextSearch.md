SQL Basics: Simple FULL TEXT SEARCH

    SELECT *
    FROM product
    WHERE to_tsvector('english', name) @@ to_tsquery('english', 'Awesome');
