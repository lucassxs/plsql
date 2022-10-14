CREATE TABLE currency (
   country         VARCHAR2(20),
   year            NUMBER,
   month           NUMBER,
   to_us           NUMBER);

INSERT INTO currency
(SELECT distinct
SUBSTR(country_name,1,20), calendar_year, calendar_month_number, 1
FROM countries
CROSS JOIN times t
WHERE calendar_year IN (2000,2001,2002)
);
UPDATE currency set to_us=.74 WHERE country='Canada';
