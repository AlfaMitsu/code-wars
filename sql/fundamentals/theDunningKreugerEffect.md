The Dunning-Kreuger Effect

    WITH overconfidence AS (
        SELECT
            id,
            name,
            perceived_skill_level - actual_skill_level AS skill_overestimation
        FROM
            users
        WHERE
            perceived_skill_level > actual_skill_level
    )
    SELECT
        id,
        name,
        skill_overestimation,
        CASE
            WHEN skill_overestimation <= 2 THEN 'Mild case of overconfidence'
            WHEN skill_overestimation <= 5 THEN 'Moderate case of overconfidence'
            WHEN skill_overestimation <= 7 THEN 'Serious case of overconfidence'
            ELSE 'Extreme case of Dunning-Kruger effect detected!'
        END AS overconfidence_category
    FROM
        overconfidence
    ORDER BY
        skill_overestimation DESC,
        id DESC;
