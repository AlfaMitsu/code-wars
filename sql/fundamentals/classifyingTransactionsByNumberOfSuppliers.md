Classifying Transactions by Number of Suppliers

    WITH transaction_supplier_count AS (
        SELECT 
            t.transaction_id,
            t.date,
            COUNT(DISTINCT tc.supplier) AS supplier_count
        FROM transaction t
        JOIN transaction_content tc ON t.transaction_id = tc.transaction_id
        GROUP BY t.transaction_id, t.date
    )
    SELECT 
        t.transaction_id,
        t.date,
        CASE 
            WHEN tsc.supplier_count > 1 THEN 'Several'
            ELSE MAX(tc.supplier)
        END AS supplier
    FROM transaction t
    JOIN transaction_content tc ON t.transaction_id = tc.transaction_id
    JOIN transaction_supplier_count tsc ON t.transaction_id = tsc.transaction_id
    GROUP BY t.transaction_id, t.date, tsc.supplier_count
    ORDER BY t.transaction_id;
