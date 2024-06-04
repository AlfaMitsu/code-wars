GROCERY STORE: Logistic Optimisation

    SELECT
      producer,
      COUNT(DISTINCT id) AS count_products_types
    FROM products
    GROUP BY producer
    ORDER BY count_products_types DESC, producer ASC;
