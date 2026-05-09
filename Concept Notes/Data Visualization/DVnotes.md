<h2>Data Visualization</h2>
-> It is used to represent data in a pictorial format like graphs and charts. <br> 
-> It can be used to interpret data patterns quickly and easily.<br>
-> It is especially useful for non-technical people to understand the data. <br>

<h3>Non-programming tools for Data Visualization</h3>
-> Tools like Excel,Power BI and Tableau Public are widely used for data visualization without programming aspects. <br>
<br>
<b>-> Advantage of using python for data visualization</b><br>
<ul>
<li>Can deal with a very large amount of data like millions of rows. (While Excel can only handle upto 2 million rows at a time)</li>
 <li>Much easier to integrate data visualizations into APIs or websites.</li> 
 <li>Much more ease of data manipulation.</li> 
</ul>

<h3>Libraries for Data Visualization in Python</h3>
-> Three common ways to visualize data: <br>
<ul>
  <li>Pandas: Utilities for basic visualization</li>
  <li>Matplotlib: The standard data visualization library</li>
  <li>Seaborn: Effective data visualization library built on matplotlib</li>
</ul>

<h3>Scatter Plot</h3>
-> Most basic plot. <br>
-> Displays points in 2D grid. <br>
-> It can be useful to find patterns, relationships and clusters. <br>

-> Some ways to create scatterplots:  
<ol>
 dSV = dataSetVariable
 <li>Pandas: dSV.plot.scatter(x="Col1",y="Col2")</li>
 <li>Matplotlib Pyplot: plt.scatter(x=dSV["Col1"], y=dSV["Col2"]) &nbsp&nbsp plt.xlabel("label") &nbsp&nbsp plt.ylabel("label") </li>
 <li>Seaborn: sns.scatterplot(data=dSV, x="Col1", y="Col2")</li>
</ol>

<h3>Line Plot</h3>
-> Plots a line between two points. Multiple such lines in the same plot/figure. <br>
-> Order of points is very important. <br>
-> For time-series plotting and relationship plotting. <br>

-> Some ways to create scatterplots:  
<ol>
 dSV = dataSetVariable
 <li>Pandas: dSV.plot.line(x="Col1",y="Col2")</li>
 <li>Matplotlib Pyplot: plt.plot(x=dSV["Col1"], y=dSV["Col2"]) &nbsp&nbsp plt.xlabel("label") &nbsp&nbsp plt.ylabel("label") </li>
 <li>Seaborn: sns.lineplot(data=dSV, x="Col1", y="Col2")</li>
</ol>

<h3>Bar Plot</h3>
-> Plots categories against numerical figures unlike scatter and line plots which use numbers on both axis. <br>
-> Useful to discover and compare relationships between categories against numerical figures. <br>
-> E.g., Gender vs Income, Marital Status vs Credit Score, etc.

-> Some ways to create bar plots:  
<ol>
 dSV = dataSetVariable
 <li>Pandas: dSV.plot.bar(x="Col1",y="Col2")</li>
 <li>Matplotlib Pyplot: plt.bar(x=dSV["Col1"], y=dSV["Col2"]) </li>
 <li>Seaborn: sns.barplot(data=dSV, x="Col1", y="Col2")</li>
</ol>

<h3>Histogram Plot</h3>
-> A special type of bar plot where the numerical figure is a count or frequency. <br>
-> Almost always vertical plots height = count/frequency of category.<br>
-> Bar plots are only possible for category vs  <br>
-> We often make histogram for numerical data by using Binning. (converting numerical data to categorical) <br>
-> For e.g., counting number of prime numbers between 0-20, 20-40, 40-60,... <br>
-> Ways to define bins: <br>
   <ol>
    <li>Manually</li>
    <li>Only specify number of bins</li>
   </ol>
->Numpy and Pandas automatically calculate size of bins using the MAX and MIN of the given data: <br>
&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp binSize = (max(X) - min(X))/bins <br>
&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp bin<sub>i</sub> = min(X) + i.binSize <br>
-> Histograms can also be used to find outliers. <br>

-> Some ways to create histogram plots:  
<ol>
 dSV = dataSetVariable
 <li>Pandas: dSV["Col1"].hist(bins=*Number of bins*)</li>
 <li>Matplotlib Pyplot: plt.hist(x=dSV["Col1"], bins=*Number of bins*) </li>
 <li>Seaborn: sns.histplot(data=dSV, x="Col1", bins=*Number of bins*)</li>
</ol>

<h3>3D plots</h3>
-> If used imporperly, these plots can be difficult to interpret and see patterns. Rotation is required and difficult to represent in ppt or docs. <br>
-> Instead, we can use color as the third dimension. <br>
&nbsp&nbsp&nbsp&nbsp Colors can represent  both numerical and categorical values. <br>
-> We can also use shapes and sizes. <br>
-> We can use color as the 3rd dimension in matplotlib, pandas and seaborn as shown in <br> 
&nbsp&nbsp&nbsp&nbsp Concept Notes/Data Visualization/coloredPlots.ipynb

<h3>Multiplots</h3>
-> Used when we want to show multiple trends, during EDA, etc. <br>
-> In pandas and matplotlib, we use subplots. <br>
-> In seaborn, we use facetgrid. <br>
-> We can use matplotlib, pandas and seaborn for getting multiple plots in one figure as shown in <br> 
&nbsp&nbsp&nbsp&nbsp Concept Notes/Data Visualization/SLBHM_Plots.ipynb




