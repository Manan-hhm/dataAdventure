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
