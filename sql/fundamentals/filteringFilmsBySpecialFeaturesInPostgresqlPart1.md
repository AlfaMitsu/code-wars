Filtering Films by Special Features in PostgreSQL: Part 1

    SELECT
        film_id,
        title,
        special_features
    FROM
        film
    WHERE
        '{Trailers,Deleted Scenes}'::text[] <@ special_features
        AND special_features @> '{Trailers,Deleted Scenes}'::text[]
    ORDER BY
        title,
        film_id;
