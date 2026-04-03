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

<h3>Data source for Pandas</h3>
-> DataFrames are often not directly created in Pandas or converted from Python lists. <br>
-> In fact, most of the DataFrames are created by reading from sources like SQL, .CSV files (most common), excel, JSON, etc. <br>
-> Another format Pickle (.pkl/.pck) can be used to transfer data between two machines. <br>
-> Pickle can be used to store data temporarily when you want to resume working on the dataset again soon.
<br> &nbsp&nbsp&nbsp&nbsp  <b>Note: </b> Pickle file format can differ by python version (a big problem)

<h3>Data types in Pandas</h3>
-> Pandas supports various data types like objects (string or mixed data like python lists, dictionaries, etc.), int64, float64, bool, datetime64, <br>  &nbsp&nbsp&nbsp&nbsp timedelta, category.

<h3>DataFrame Indices</h3>
-> Can be simple integers starting from 0/1 but not necessarily. <br>
-> You can set a column as the index of a Dataframe, making them more similar to dictionaries than lists. <br>
-> Dataframe rows can be accessed using loc or iloc (iloc is based on location number not index).

<h3>Masks</h3>
-> Masking is used to select from a dataframe. We can create mask based on some conditions to fetch specific data. <br>
-> We can use logical operators like AND, OR, NOT to mask based on multiple conditions as desired. <br>
-> For example: (df['t'] == 'a') | (df['t'] == 'b') | (df['t'] == 'c'). This would return a Boolean series. <br>
-> Direct/default masking returns a boolean series: <br>
&nbsp&nbsp&nbsp&nbsp countries_covid_data["Country"] == "India" <br>
-> Pass the mask as a column-like reference to display data: <br>
&nbsp&nbsp&nbsp&nbsp countries_covid_data[(countries_covid_data["Country"] == "India")] <br>
-> In newer Pandas versions we can simply use query to mask and display output: <br>
&nbsp&nbsp&nbsp&nbsp countries_covid_data.query("(Country == 'India') & (Date == '2020-06-22')") 

<h3>NULL/Missing values</h3>
-> Data often has blank values. <br>
-> Panda often fills these blanks with "NaN" or "None". <br>
-> NaN: Not a Number. Fill blank values in numerical columns. <br>
-> None: Python's equivalent of NULL. Fill blanks for object type columns. <br>
-> NaT: Not a Time. Fill blank values in datetime columns. <br> <br>

-> Not all blank values will be NaN/None. <br>
-> Often an invalid value may be used. (E.g.: Age is unknown:  using -1/0  or Name unknown: using empty string "") <br>
-> Use .str.strip() to remove blank spaces like " ", "  ".

<h3>Joining/Merging DataFrames</h3>
Five types of join/merge: <br>
1. INNER: Only rows present on both dataframes are kept. (e.g. Join Country Covid data with Continent data) <br>
2. LEFT: Rows present on both dataframes are kept, along with leftover rows from the left dataframe. (e.g. Hong Kong considered in country covid <br> &nbsp&nbsp&nbsp data but not in continent country data.) <br>
3. RIGHT: Rows present on both dataframes are kept, along with leftover rows from the right dataframe. <br>
4. OUTER JOIN: Rows present on both dataframes are kept, along with leftover rows from both the left and right dataframes. (e.g. Vatican City <br> &nbsp&nbsp&nbsp considered with NULL data values in Covid data and has existence in Country Continent data) <br>
5. ANTI-JOIN: Rows present on both dataframes are removed, only leftover rows from botht the dataframes are kept. <br>
&nbsp&nbsp&nbsp ANTI-LEFT & ANTI-RIGHT to keep only left and right leftover rows respectively. <br> &nbsp&nbsp&nbsp
(E.g. Anti-join finds out that many small countries in Europe have covid data missing. It can be reported to the data
collection team about <br> &nbsp&nbsp&nbsp missing data.)
