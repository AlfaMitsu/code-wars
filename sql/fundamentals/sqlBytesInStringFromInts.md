SQL: Bytes in String from Ints

    SELECT
        OCTET_LENGTH(number1::text) AS octnum1,
        OCTET_LENGTH(number2::text) AS octnum2,
        OCTET_LENGTH(number3::text) AS octnum3,
        OCTET_LENGTH(number4::text) AS octnum4,
        OCTET_LENGTH(number5::text) AS octnum5
    FROM
        numbers;
