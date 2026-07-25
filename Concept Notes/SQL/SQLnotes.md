<h3>SQL/Structured Query Language</h3>
-> An important type of tool used in almost every major company to create, maintain, and fetch data. <br>
-> It is mainly used because it is easy to use and maintain, and can be made to be really fast. <br>
-> It is not a programming language. But a form of it: PL/SQL is similar to programming.<br>
-> Data Scientists use SQL for fetching data. <br> <br>

-> It is not a unified language. It can be implemented in many ways/types like MsAccess, MySQL, Postgres, SQLite, etc. <br>
-> MySQL is an open-source tool which implements SQL. <br>
-> Syntax and concepts between these types are very similar. <br>
-> However, specific features are available to certain tools. For e.g., BigQuery has lists, araays, etc. unlike MySQL, etc. <br>

<h4>SQL Terminologies</h4>

<b>Database: </b> An entire collection of data stored in tables. <br>
<b>Table: </b> A table containing our required data, similar to an Excel or pandas DataFrame. <br>
<b>Row: </b> A row in the table, similar to a row in DataFrame. <br>
<b>SQL Statement/SQL Query: </b> An instruction we use to fetch/change/work with data in the database. <br>

<h4>SQL Statement Types</h4>
<b>-> Two main types: </b>
-> <b>Data Definition Language(DDL): </b> Used to define and create SQL databases. <br>
-> Example: CREATE <br>
-> <b>Data Manipulation Language(DML): </b> Used to manipulate and fetch data in databases. <br>
-> Example: SELECT for fetching data, INSERT for manipulation/entry of data. <br>

<h4>MySQL data types</h4>

-> Different columns can have different but fixed data types in each one of them. <br>
-> Main types used are: VARCHAR, LONGTEXT, INT, BIGINT, FLOAT, DOUBLE, DATE, DATETIME, TIMESTAMP, BOOLEAN. <br>

<h4>SELECT</h4>
-> Statement to fetch data. <br>
-> We can choose which columns to fetch the data from, how many rows to fetch and how they should be ordered by keywords 
like &nbsp&nbsp&nbsp&nbsp "order by" and "limit" <br><br>

-> We use * to select and retrieve data from all the columns. <br>
-> Syntax: SELECT * FROM tableName <br> 
-> Example: SELECT * FROM city <br> <br>

-> We use column names separated by commas to retrieve data from specific columns only. <br>
-> Syntax: SELECT Column1, Column2,...ColumnN FROM tableName <br>
-> Example: SELECT city, country_id FROM city <br><br>

-> We can limit no. of rows retrieved by using LIMIT keyword. <br>
-> Syntax: SELECT * FROM tableName LIMIT numericalValue <br>
-> Example: SELECT * FROM city LIMIT 10<br> <br>

-> We can use ORDER BY keyword to order rows based on specific column. <br>
-> Syntax: SELECT * FROM tableName ORDER BY columnName <br>
-> Example: SELECT * FROM city ORDER BY country_id LIMIT 100<br>
-> <b>Note:</b> ORDER BY comes before LIMIT. We don't have to SELECT the column which we are ordering by.<br><br>
-> We can use rand() function in ORDER BY to get random items (for example as samples) from a table. <br>
-> Example: SELECT * FROM city ORDER BY rand() LIMIT 100<br>


