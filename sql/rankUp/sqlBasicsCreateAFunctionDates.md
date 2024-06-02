SQL Basics: Create a FUNCTION (DATES)

    CREATE OR REPLACE FUNCTION agecalculator(birthdate DATE)
    RETURNS INTEGER AS $$
    BEGIN
        RETURN EXTRACT(YEAR FROM age(NOW(), birthdate));
    END;
    $$ LANGUAGE plpgsql;
