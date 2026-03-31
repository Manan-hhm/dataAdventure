<h3>Numpy (np) </h3>
-> A python library that is fundamental for data science. <br>
-> Almost all the other data science libraries use/based on Numpy. <br>
-> Deals with vectors and matrices (building blocks of data science algos.) <br>
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
<b>->array: </b> Create an array from passed parameter. <br> &nbsp&nbsp&nbsp&nbsp A single datatype per array is recommended. For  different datatypes, it will try automatic conversions like int to float or int/float to string. <br>
<b>-> shape: </b> Returns no. of lists inside lists and no. of elements in inner lists. <br>
<b>-> arange(n): </b> Create an array from 0 to n-1.<br>
<b>-> zeros(shape): </b> Create an array with all 0s as per defined shape.<br>
<b>-> ones(shape): </b> Create an array with all 1s as per defined shape.<br>
<b>-> random.randint(range, size=shape): </b> Create an array with defined<br>
<b>-> astype: </b> Convert numpy array data type (e.g. float to int32)
-> Code example: Concept Notes/Numpy/NumpyArrs.ipynb

<h3>Numpy data types</h3>
-> int (8, 16, 32, 64 bits), uint (8, 16, 32, 64 bits), bool, float (16, 32, 64, 128 bits)

<h3>Numpy array slicing</h3>
-> Reducing or masking arrays to obtain smaller arrays as desired. <br>

<h3>Transpose</h3>
-> Transposing a matrix converts its rows into columns and columns into rows. <br> 
-> The order of the resultant matrix thus can get reversed in case of a rectangular matrix. <br>
-> It can be used to centre matrix operations around parameters that are in columns without transposing. <br>
&nbsp&nbsp&nbsp&nbsp Because transposing gets those parameters in row arrangement. (Refer to the code example in Transpose.ipynb) <br>

<h3>Broadcasting</h3>
-> It allows operations on arrays of different dimensions. <br>
-> For example, a 3x1 matrix A can be added to a 3x4 matrix B by broadcasting (converting A into a 3x4 matrix by repeating the same elements &nbsp&nbsp&nbsp&nbsp as column 1 through all its 4 columns) <br>
-> Conditions: Number of rows must be same for both the matrices. The matrix used to perform an operation on the main matrix must have only &nbsp&nbsp&nbsp&nbsp 1 column. <br>
-> Very important. We often need to add additional numbers to an entire matrix. <br>
&nbsp&nbsp&nbsp&nbsp For example, in neural networks, we add bias vector to multiplication of input and weight vectors by broadcasting.

<h3>Matrix Multiplication</h3>
-> A significant operation used almost everywhere in ML, especially in Neural networks/Deep learning. <br>
-> GPUs are used to accelerate matrix multiplication. <br>
-> For example, we want to calculate final grades of student based on weightage of each subject. (similar to weight matrix in neural networks) <br>
-> 3x4 matrix: 3 students 4 subjects. 4x1 matrix: weightage of each subject <br>
-> Multiplication result: Final grade/score of each student in a 3x1 matrix. <br>
-> For multiplying any two matrices A (of order MxN) and B (of order PxQ): <br>
&nbsp&nbsp&nbsp&nbsp No. of columns of A and no. of rows of B must be the same .i.e. N = P.
