W.R.T MySQL engine
<h2>For retrieving values within a list: </h2>
>SELECT .... FROM .... WHERE name IN ('n1', 'n2', ...) <br><br>

<h2>For finding values that match patterns: </h2>
>SELECT .... FROM .... WHERE name LIKE '%a' OR name LIKE 'a%' OR name LIKE '%a%' <br><br>

<h2>For rounding values: </h2>
Round to positive decimal places (e.g., 12003.03456 -> 12003.03): <br> 
>SELECT name, round(gdp/population, 2) FROM world WHERE ..... <br><br>
Round backwards to nearest places (e.g., 1200343 -> 1200000 or 120990 -> 121000): <br>
>SELECT name, round(gdp/population, -3) FROM world WHERE ..... <br><br>


<h2>Isolating left characters: </h2>
>SELECT .... FROM .... WHERE LEFT(name, 1) = LEFT(surname, 1) <br><br>

<b>Note: </b> NOT EQUALS symbol is <> <br><br>

<h2>Giving boundary including ranges: </h2>
E.g.: SELECT .... FROM .... WHERE number BETWEEN 10 AND 30 <br>

<b>Note: </b> Umlaut -> Ü is typed by enabling num lock and then holding alt while entering following <br>
decimal number on the numpad 0 2 2 0 and then releasing the held key/s. <br><br>

<h2>Listing some elements last: </h2>
The IN operator can be used to display values like 0/1 as well. <br>
For example: SELECT SUBJECT IN ('Physics', 'Chemistry') FROM..... will return 0/1 depending upon whether the subject 
is in the list (1) or not (0) <br>

The same can be used in ORDER BY to display the subjects of the list at last. <br>
Example: SELECT winner, subject <br>
  FROM nobel <br>
 WHERE yr=1984 <br>
 ORDER BY subject IN ('Physics','Chemistry'),subject,winner <br>

 <b>Note: </b> This does not work in some SQL variations like Microsoft SQL. It doesn't allow Boolean value in syntax. <br>
 We can instead use CASE WHEN....THEN....ELSE...END <br>
 like CASE WHEN subject IN ('Physics','Chemistry') THEN 1 ELSE 0 END <br>
 We can use it in MySQL and PostgreSQL too.<br>
 However, in PostgreSQL, make sure the listed items are in correct cases because it is case-sensitive.<br>

