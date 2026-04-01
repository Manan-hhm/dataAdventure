<h2>Pandas</h2>
-> Pandas is a library used to read and manipulate data.<br>
-> It uses Numpy library as a foundational dependency to make operations fast. <br>
-> It is like the second layer in what we think of as ML pipeline. <br>
-> It is used to read and process and make data ready for use in ML. <br>
-> It is similar to using SQL but more powerful in some use cases (like in ML).

<h3>When do we use Pandas?</h3>
-> Read and process tabular data from files like .CSV locally or cloud or read from SQL. <br>
-> Join multiple data files (like several .CSV files to append, join, etc.) <br>
-> Removing invalid or wrong data (useful in analytics) <br>
-> Calculating business relevant numbers on matrix (an important and common use case) <br>
-> Feature engineering for ML use cases.

<h3>When to not use Pandas?</h3>
-> For non-tabular data like images or text. <br>
-> Not for very large data (>3GB) as it is not multithreaded. (For large data sizes, use Spark or SQL) <br><br>
<b>Large companies have large amounts of data. Then why learn Pandas? </b> <br>
-> (i)&nbsp Data is compressed to suit to Pandas. <br>
-> (ii) Everything learned as concept in Pandas is directly applicable when learning things like Spark or SQL. <br>
&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp So, it is good as a foundational knowledge that can be transferred. 

<h3>Dataframe & Series</h3>
-> Dataframes are basically tables in Pandas. <br>
-> Every DataFrame is made up of series. <br>
-> Each Series is equivalent to a column vector.
-> Functions like head, tail, info etc. allow us to see inside a Pandas DataFrame.
