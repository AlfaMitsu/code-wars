Successful Film Stars Analysis

    WITH film_rental_counts AS (
        SELECT
            f.film_id,
            COUNT(r.rental_id) AS rental_count
        FROM
            film f
            LEFT JOIN inventory i ON f.film_id = i.film_id
            LEFT JOIN rental r ON i.inventory_id = r.inventory_id
        GROUP BY
            f.film_id
    ),
    actor_film_counts AS (
        SELECT
            fa.actor_id,
            COUNT(DISTINCT fa.film_id) AS film_count
        FROM
            film_actor fa
            JOIN film_rental_counts rc ON fa.film_id = rc.film_id
        GROUP BY
            fa.actor_id
    ),
    actor_rental_counts AS (
        SELECT
            fa.actor_id,
            SUM(rc.rental_count) AS total_rentals
        FROM
            film_actor fa
            JOIN film_rental_counts rc ON fa.film_id = rc.film_id
        GROUP BY
            fa.actor_id
    ),
    valid_actors AS (
        SELECT
            afc.actor_id,
            a.first_name || ' ' || a.last_name AS full_name,
            afc.film_count
        FROM
            actor_film_counts afc
            JOIN actor a ON afc.actor_id = a.actor_id
            JOIN actor_rental_counts arc ON afc.actor_id = arc.actor_id
        WHERE
            afc.film_count >= 20
            AND NOT EXISTS (
                SELECT 1
                FROM film_rental_counts rc
                WHERE rc.rental_count < 7 AND rc.film_id IN (
                    SELECT film_id FROM film_actor WHERE actor_id = afc.actor_id
                )
            )
    )
    SELECT
        actor_id,
        full_name,
        film_count
    FROM
        valid_actors
    ORDER BY
        film_count DESC,
        actor_id ASC;
