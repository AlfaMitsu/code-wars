SQL Basics: Simple NULL handling

    SELECT
      id,
      COALESCE(NULLIF(name, ''), '[product name not found]') AS name,
      price,
      COALESCE(NULLIF(card_name, ''), '[card name not found]') AS card_name,
      card_number,
      transaction_date
    FROM
      eusales
    WHERE
      price IS NOT NULL
      AND price > 50.00;
