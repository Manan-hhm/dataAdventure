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

 <h2>SELECT in SELECT</h2>
<ol>
  <li>To compare numerically: <br> SELECT...FROM....WHERE a>(SELECT a FROM....WHERE....)<br>
  SELECT name FROM world
  WHERE population >
     (SELECT population FROM world
      WHERE name='Russia')
  <br>
  </li>
  <li>ALL statement for comparing to more than one rows: <br>
     SELECT...FROM....WHERE a>ALL(SELECT a FROM....WHERE....)<br>
   Example: SELECT name <br>
FROM world <br>
WHERE gdp > ALL(SELECT gdp FROM world WHERE gdp>0 AND continent ='Europe')
  <br></li>
  <li>To search in list: <br> SELECT...FROM...WHERE a IN (SELECT a FROM....WHERE....)<br>
  SELECT name, continent FROM world
    WHERE continent IN 
    (SELECT continent FROM world WHERE name = 'Argentina' OR name = 'Australia')<br></li>
  <li>As a part of the columns to show: <br> SELECT a, b/(SELECT b FROM...WHERE...) FROM...WHERE....<br>
  SELECT name, CONCAT(ROUND((population*100/(SELECT population FROM world WHERE name = 'Germany')), 0),'%') AS 'percentage' <br>
    FROM world WHERE continent = 'Europe'<br>
  <b>Note: </b> Here, we used CONCAT(a,b) function to join two strings for showing the % symbol in results.<br>
  <b>Alternative way:</b><br>
  WITH pog AS (SELECT population FROM world WHERE name ='Germany') <br>
SELECT name, CONCAT(ROUND(population*100/(SELECT population FROM pog),0),'%') <br>
FROM world WHERE continent = 'Europe'
  <br></li>
  <li>We can refer to values in the outer SELECT within the inner SELECT. <br>
    We can name the tables so that we can tell the difference between the inner and outer versions<br>
  Example: SELECT continent, name, area FROM world x <br>
  WHERE population >= ALL <br>
    (SELECT population FROM world y <br>
        WHERE y.continent=x.continent <br>
          AND population>0) <br> 
    The above example is known as a correlated or synchronized sub-query <br>
  </li> 
  <li>To compare alphabetically: <br> SELECT...FROM....WHERE a>(SELECT a FROM....WHERE....)<br>
 SELECT continent, name <br>
FROM world x <br>
WHERE name <= ALL(SELECT name FROM world y WHERE y.continent = x.continent) <br>
  </li>
  When all the values of a group have to satisfy some condition: <br>
  Example: Find the continents where all countries have a population <= 25000000. <br> 
    Then find the names of the countries associated with these continents. Show name, continent and population. <br>
  Query: SELECT name, continent, population <br>
FROM world <br>
WHERE continent IN <br> 
(SELECT continent FROM world GROUP BY continent HAVING MAX(population) <= 25000000) <br>
  <b>Note: </b> when a condition applies to a group as a whole, you need HAVING inside a subquery, not WHERE on the outer query. <br>
  WHERE filters individual rows before grouping, and HAVING filters groups after grouping. <br>
  <li>
    When row needs to be compared against other rows of its group: <br>
    Example: Some countries have populations more than three times that of all of their neighbours (in the same continent). <br> Give the countries and continents. <br>
    Query: SELECT DISTINCT x.name, x.continent <br>
FROM world x <br>
WHERE x.population > <br>
3*(SELECT MAX(y.population) <br>
FROM world y <br>
WHERE y.continent = x.continent AND <br>
y.name != x.name) <br>
  </li>
</ol>
