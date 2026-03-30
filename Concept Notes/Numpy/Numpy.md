<h3>Numpy (np) </h3>
-> A python library that is fundamental for data science.
-> Almost all the other data science libraries use/based on Numpy.
-> Deals with vectors and matrices (building blocks of data science algos.)
-> Data can be shared during ML processes and other operations in np arrays.

<h4>Features</h4>
-> Optimized for numerical data operations. <br>
-> Written in C. So, it is optimized for speed. <br>
-> Lots of submodules for doing tasks like matrix multiplications, chi-test, matrix decomposition, etc. useful in data science tasks. <br>
-> Some unique things to handle non-numerical data, infinities, etc.

<h4>Disadvantages</h4>
-> Not directly useful for majorly non-numerical data (e.g. reviews). <br>
-> Runs on CPU. Not useful for work done on GPU (like deep learning).

<h3>Vector and Matrices</h3>
<b>-> Vector: </b> List of Numbers <br>
<b>-> Matrices: </b> List of vectors  

<h3>Some numpy functions</h3>
<b>array: </b> Create an array from passed parameter. <br> A single data type per array is recommended. If you provide different datatypes, it will try automatic conversions like int to float or int/float to string. <br>
<b>shape: </b> Returns no. of lists inside lists and no. of elements in inner lists. <br>
<b>arange(n): </b> Create an array from 0 to n-1.<br>
<b>zeros(shape): </b> Create an array with all 0s as per defined shape.<br>
<b>ones(shape): </b> Create an array with all 1s as per defined shape.<br>
<b>random.randint(range, size=shape): </b> Create an array with defined<br>
<b>astype: </b> Convert numpy array data type (e.g. float to int32)

<h3>Numpy data types</h3>
int (8, 16, 32, 64 bits), uint (8, 16, 32, 64 bits), bool, float (16, 32, 64, 128 bits)

<h3>Numpy array slicing</h3>
Reducing or masking arrays to obtain smaller arrays as desired.

<h3>Transpose</h3>
Transposing a matrix converts its rows into columns and columns into rows. <br> 
The order of the resultant matrix thus can get reversed in case of a rectangular matrix. <br>
It can be used to centre matrix operations around parameters that are in columns without transposing. <br>
Because transposing gets those parameters in row arrangement.
