    1. Find the author with the name 'Kara Melton' and then select all the articles she has written.

    SELECT id FROM authors WHERE name='Kara Melton';
    SELECT * FROM articles WHERE author_id=8;

    2. Find Ontario in the provinces table and then find all the cities in that province.

    SELECT id FROM provinces WHERE name='Ontario';
    SELECT * FROM cities WHERE province_id =14;

    3. Who wrote the article called 'Coding Bootcamps and Emotional Labor'?

    SELECT author_id FROM articles WHERE title='Coding Bootcamps and Emotional Labor';
    SELECT name FROM authors WHERE id=4;
    Tilde Ann Thurium

    4. Write a series of SQL queries to find out how many provinces are in Canada.

    SELECT id FROM countries WHERE name='Canada';    (id = 1)
    COUNT * FROM provinces WHERE country_id=1;
    SELECT COUNT(country_id=1) FROM provinces;
    14

    5. How many people live at 4740 McDermott Street?

    SELECT id FROM residences WHERE address='4740 McDermott Street';
    id=9
    SELECT COUNT(residence_id=9) FROM persons;
    100

     ?? SELECT residence_id FROM persons WHERE id=9;   (returns residence_id 4)

    6. What city is 4740 McDermott Street in?

    SELECT city_id FROM residences WHERE address='4740 McDermott Street';
    SELECT name FROM cities WHERE id=11;
    Ottawa

    7. What province is 4740 McDermott Street in?

    SELECT province_id FROM cities WHERE id=11;
    SELECT name FROM provinces WHERE id=14;
    Ontario

    8. What country is 4740 McDermott Street in?

    SELECT country_id FROM provinces WHERE id=14;
    SELECT name FROM countries WHERE id=1;

    9. Find the person named 'Destini Davis' and then use a series of SQL queries to find what country they live in.

    SELECT residence_id FROM persons WHERE name='Destini Davis';
    SELECT city_id FROM residences WHERE id=2;   (city_id = 8)
    SELECT name FROM cities WHERE id=8;
    Destini lives in Toronto, Canada

    10. How many articles has Aditya Mukerjee written?

    SELECT id FROM authors WHERE name='Aditya Mukerjee';
    SELECT author_id FROM articles WHERE id=2;
    SELECT COUNT(author_id) FROM articles WHERE author_id=2;
