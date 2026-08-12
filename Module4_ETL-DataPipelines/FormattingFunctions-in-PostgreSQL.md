# Inserting Data and Formatting Functions in PostgreSQL
## INSERT INTO TABLE AS QUERY RESULT:

We can insert new records into an existing table by using the results of the SQL query of another table.Here the contents of the table are populated with the data computed by the result of a SELECT statement on another table.

Syntax:

INSERT INTO table_name [(column_name)] AS QUERY

Example

INSERT INTO movie_release(movie_name,movie_cast,dateofrelease) AS select movie_name, movie_cast, dateofrelease from movies

 In this example, movie_release is the table whose value is populated from the values present in movies table.    

## Data Type formatting functions in PostgreSQL:

Sometimes we need to convert various data types, such as date/time, integer, floating point etc., into formatted strings. These functions consider two arguments: the first argument is the value we need to format, and the second argument will be the template that defines the format.

Here we will discuss timestamp formatting using the to_char function.

Syntax

to_char(timestamp,text)

This converts the given timestamp into the given format.

Example, on executing this query below:
select to_char(timestamp '2002-04-20 17:31:12.66', 'HH12:MI:SS')

we get the output as 05:31:12

Similarly, we can apply various formatting options for timestamp such as:

    HH12 : displays hour of day(0-12)

    HH24 : displays hour of day(0:23)

    MI: displays minute(0:59)

    SS:displays second(0:59)

    MON:month name in upper case

    mon:month name in lower case.

    DAY:full upper case day name

    day:full lower case day name

    year:year in YYYY will be year data.
