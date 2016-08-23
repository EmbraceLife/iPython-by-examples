# iPython-by-exmaples


## **Tasks**
**Use Bokeh Movies example**
- which stocks rise 5 times or more over last 10 years? 
- which stocks rise 5 times or more since 2007's high? 
- What are their distinguished features compared to other stocks?
- try out every and each important features to find out the interesting ones   



## **Table of Content**

  

## M2 vs Stocks
[Where to find bokeh dataset locally?](#bokeh-datasets)    
[How to download specific folder from a github repo?](#repo-folder)    
[How to print out stock data info nicely?](#stock-print-nicely)    
[How to get daily, weekly, monthly stock data?](#daily-weekly-monthly-data)    
[How to turn codes into a function to easily change a parameter?](#make-func)    
[How to do basic statistics like `mean()`?](#statistics)    
[How to fill up columns with 0s with `len(), range(), .iat()`](#fill-up-column)    
[How to use for in loop with range?](#for-in-range)    
[How to create a dataframe from scatch?](#dataframe-from-scratch)   
[How to tranform a column of a dataframe?](#create-column)    
[How to create an empty dataframe?](#create-empty-dataframe)        
[How to search and use unpaid dataAPI?](#unpaid-api)    
[How to read first/last 10 rows of a dataframe?](#first-n-rows)    
[How to convert a column of a dataframe to a list?](#column-to-list)    
[How to get all stock names which can be borrowed to sell?](#borrow-sell)     
[How to convert "2016-08-12" to "20160812"?](#transform-date-string)    
[How to filter out rows using a column?](#filter-out-rows)    
[How to access all trading calendar date of ShangHai market?](#trading-date-shanghai)    
[How to import libraries](#import-lib)    
[How to save dataframe to csv file?](#save-csv)    
[How to access a column of a dataframe?](#access-column)    
[How to plot M2-10-year change?](#m2-10years-plot)    
[How to search and use DataAPI?](#search-use-dataapi)    
[How to read a tsv file?](#read-tsv)    
[How to read dirty file](#read-dirty-file)    
[How to read csv file?](#read-csv)    
[How to read dirty file ignoring pre and post comment?](#read-dirty-comment-file)    
[How to use jupyter notebook?](#jupyter)    
[What is a dataframe and a pandas series?](#dataframe-series)      
[How to know an object's type?](#get-type)   
[How to check basic summary of a dataframe?](#data-summary)    
[How to understand function, method and attributes to a dataframe or series?](#func-method-attribute)    
[How to get the types of all columns of a dataframe?](#dtypes)     
[How to check a function's api?](#check-api)      
[How to install and update libraries, diff versions?](#install-update-libraries)     
[How to rename columns of a dataframe?](#rename-columns)    
[How to remove columns of a dataframe?](#remove-columns)    
[How to remove rows of a dataframe?](#remove-rows)
[How to check the structure of a dataframe?](#structure-dataframe)    
[How to sort a column or a dataframe?](#sort-dataframe)    
[How to fill a list using for in loop and append?](#fill-list)    
[How to check length of a list?](#length-list-dataframe)    
[How to convert a list to a series?](#list-to-series)    
[How to filter rows of a dataframe?](#filter-rows)    
[How to filter by multiple conditions on columns?](#more-fitlers)    
[How to work on or and and?](#or-and)    
[How to only read certain columns of dataframe?](#read-specific-columns)      
[How to only read certain rows of dataframe?](#read-specific-rows)    
[How to iterate a series (like a list)?](#iterate-series)    
[How to iterate a dataframe by rows?](#iterate-dataframe)    
[How to drop all non-numeric columns or only keep numeric columns of a dataframe?](#numeric-columns)    
[How to describe only numeric, all, or specific columns of a dataframe?](#describe-dataframe)    
[How to understand use of `inplace=True` in drop columns and rows of a dataframe?](#drop-inplace)    
[How to refer to rows and columns with axis=0,1,'index','column'?](#axis-row-column)    
[How to use string methods upper, contains, replace in pandas?](#string-methods)    
[How to create a random array and test type?](#random-nparray-type)    
[How to get the type of an object?](#type)    
[How to create a small dataframe?](#create-dataframe)    
[How to row-bind dataframe?](#row-bind-dataframe)    
[How to access a stock daily data?](#stock-daily)    
[How to plot a stock series out of the stock dataframe?](#plot-stock-series)     
[How to calc return from a price series?](#stock-series-return)    
[How to plot histogram out of a price series?](#histogram-stock-return)    
[How to use numpy statistics on numpy array?](#stats-array)    

## part2   
[Three ways to create a figure or graph](#create-a-figure)    
[How to create a random table of data but not a dataframe?](#numpy-random-table)    
[How to create a simple numpy array?](#create-numpy-array)    
[How to create an array range from 0 to 99?](#create-numpy-array-range)
[How to change an array to a table?](#array-to-table)    
[How to turn a single array to multi-dim table?](#array-to-multi-dim-table)     
[How numpy array select by index?](#numpy-index)    
[How numpy array select on condition?](#condition-selection)        
[how to create array with specific range and intervals?](#numpy-array-range-intervals)      
[How to create a table by multiply a row array and a column array?](#row-multiply-column)       
[How to find out the version and backend of matplotlib?](#matplotlib-version)    
[How to plot graph inside jupyter cell?](#matplotlib-inline)    
[How to create an empty graph?](#empty-graph)        
[how to create a graph with double tall than wide?](#empty-graph-double-height)     
[How to create a graph with axis, title and label?](#create-axis-title-label)        
[How to create a graph with line plot and scatterplot?](#line-scatterplot)    
[How to create multiple graphs on a chart?](#multiple-charts)       
[Three ways to create a figure or graph](#create-a-figure)    
[How to set random seed?](#seed-array-figure-barchart-axisLine)     
[How to create numpy arrays?](#seed-array-figure-barchart-axisLine)    
[How to create a 1row-2column figure?](#seed-array-figure-barchart-axisLine)    
[How to create horizontal-vertical barchart?](#seed-array-figure-barchart-axisLine)    
[How to create horizontal-vertical lines?](#seed-array-figure-barchart-axisLine)    
[How to create a single empty figure?](#seed-array-figure-barchart-axisLine)    
[How to create a single barchart for a subplot?](#seed-array-figure-barchart-axisLine)    
[How to loop all to select certain bars and change them?](#seed-array-figure-barchart-axisLine)         
[How to access a single bar's x and y values?](#seed-array-figure-barchart-axisLine)        
[1. How to create a 100 random number and cumsum them?](#seed-array-figure-barchart-axisLine)        
[2. How to create a 100 equal spaced numbers between 0 and 99?](#seed-array-figure-barchart-axisLine)        
[3. How to create a areaChart or fill_between chart between y value and 0?](#seed-array-figure-barchart-axisLine)        
[4. How to create straight lines and curve line?](#seed-array-figure-barchart-axisLine)        
[5. Plot the envelope with `fill_between`](#seed-array-figure-barchart-axisLine)        
[6. Plot the "centerCurveline" with `plot`](#seed-array-figure-barchart-axisLine)        
[1. How to create custom x, y arrays?](#example3)      
[2. How to convert array to a table of 100 columns?](#example3)        
[3. How to get min value for each row of table?](#example3)       
[4. How to get mean value for each row of table?](#example3)      
[5. How to get max-min value for each row of table?](#example3)       
[6. How to create two straight lines in x and y coords?](#example3)      
[7. How to create a line using x and y arrays?](#example3)           
[8. How to create barchart with error lines?](#example3)       
[9. How to create areaChart between two straight lines?](#example3)        
[10. How to set title, labels](#example3)      
[1. import a func to get data from matplotlib.cbook](#example4)    
[2. load data with numpy func](#example4)     
[3. create a single figure?](#example4)      
[4. How to create color map with numpy table like array?](#example4)    
[5. How to add color map legend?](#example4)     
[video: colormap](https://youtu.be/IF1n9TA1dO0)    
[1. How to create a legend box for a colormap graph?](#example5)    
[2. How to create a colormap with a color style?](#example5)    
[3. How to create colormap legend using a custom legend box?](#example5)    
[1. How to create a colormap with different color style and display as blocks?](#example6)    
[2. How to create a colormap legend by default?](#example6)    
[1. How to set value-min and value-max to be symmetric?](#example7)    
[1. How to create 3 custom 10x10 random tables with numpy array?](#example8)    
[2. How to create a figure with 3 subplots and leave some space for legend?](#example8)    
[3. How to set padding for figure and subplots?](#example8)    
[4. How to loop every subplots and datasets and create a colormap for each?](#example8)    
[1. How to create 3 lines altogether?](#speakMPL)     
[Frequently used color names for bokeh and all color names ?](#color-bokeh)    
[marks used by bokeh](#markers)    


### Markers
[Markers](http://matplotlib.org/api/markers_api.html) are commonly used in [`plot()`](http://matplotlib.org/api/pyplot_api.html#matplotlib.pyplot.plot) and [`scatter()`](http://matplotlib.org/api/pyplot_api.html#matplotlib.pyplot.scatter) plots, but also show up elsewhere. There is a wide set of markers available, and custom markers can even be specified.

marker     |  description  ||marker    |  description  ||marker    |  description  ||marker    |  description  
"."        |  point        ||"+"       |  plus         ||","       |  pixel        ||"x"       |  cross
"o"        |  circle       ||"D"       |  diamond      ||"d"       |  thin_diamond ||          |
"8"        |  octagon      ||"s"       |  square       ||"p"       |  pentagon     ||"\*"      |  star
"&#124;"   |  vertical line||"\_"      | horizontal line ||"h"     |  hexagon1     ||"H"       |  hexagon2
0          |  tickleft     ||4         |  caretleft    ||"<"       | triangle_left ||"3"       |  tri_left
1          |  tickright    ||5         |  caretright   ||">"       | triangle_right||"4"       |  tri_right
2          |  tickup       ||6         |  caretup      ||"^"       | triangle_up   ||"2"       |  tri_up
3          |  tickdown     ||7         |  caretdown    ||"v"       | triangle_down ||"1"       |  tri_down
"None"     |  nothing      ||`None`    |  nothing      ||" "       |  nothing      ||""        |  nothing


### color bokeh
- b: blue
- g: green
- r: red
- c: cyan
- m: magenta
- y: yellow
- k: black
- w: white
[full list](http://www.w3schools.com/html/html_colornames.asp)

### speakMPL
```python
from __future__ import print_function
# Turning on inline plots -- just for use in ipython notebooks.
import matplotlib
matplotlib.use('nbagg')
import numpy as np
import matplotlib.pyplot as plt

t = np.arange(0.0, 5.0, 0.2)

# 1. How to create 3 lines altogether? 
plt.plot(t, t,  t, t**2,  t, t**3 )
plt.show()
```



### bokeh datasets
- Users -> Natsume -> .bokeh



### repo folder   
```
svn checkout https://github.com/githubUserName/repoName/trunk/folderName
svn checkout https://github.com/EmbraceLife/bokeh/trunk/examples
```

### example8
```python
import numpy as np
import matplotlib.pyplot as plt
np.random.seed(1)

# 1. How to create 3 custom 10x10 random tables with numpy array?
data1 = np.random.random((10, 10))
data2 = 2 * np.random.random((10, 10))
data3 = 3 * np.random.random((10, 10))

# 2. How to create a figure with 3 subplots and leave some space for legend?
fig, axes = plt.subplots(nrows=3, figsize=plt.figaspect(2))

# 3. How to set padding for figure and subplots?
fig.tight_layout() # Make the subplots fill up the figure a bit more...

cax = fig.add_axes([0.85, 0.1, 0.03, 0.8]) # Add an axes for the colorbar

# 4. How to loop every subplots and datasets and create a colormap for each?
for ax, data in zip(axes, [data1, data2, data3]):
    im = ax.imshow(data, vmin=0, vmax=3, interpolation='nearest')

fig.colorbar(im, cax=cax, orientation='vertical')
plt.show()
```


### example7   
```python
fig, ax = plt.subplots()

# 1. How to set value-min and value-max to be symmetric? 
im = ax.imshow(data, cmap='seismic', interpolation='nearest',
               vmin=-2, vmax=2)
fig.colorbar(im)
plt.show()
```



### example6  
```python

from matplotlib.cbook import get_sample_data
# data = np.load(get_sample_data('axes_grid/bivariate_normal.npy'))

fig, ax = plt.subplots()

# 1. How to create a colormap with different color style and display as blocks?
im = ax.imshow(data, cmap='seismic', interpolation='nearest')

# 2. How to create a colormap legend by default?
fig.colorbar(im)
plt.show()
```

### example5   
```python
fig, ax = plt.subplots()

# 1. How to create a legend box for a colormap graph?
cax = fig.add_axes([0.27, 0.2, 0.05, 0.6])

# 2. How to create a colormap with a color style? 
im = ax.imshow(data, cmap='gist_earth')

# 3. How to create colormap legend using a custom legend box? 
fig.colorbar(im, cax=cax, orientation='vertical')

plt.show()
```

### example4
```python
# 1. import a func to get data from matplotlib.cbook
from matplotlib.cbook import get_sample_data

# 2. load data with numpy func 
data = np.load(get_sample_data('axes_grid/bivariate_normal.npy'))
print(data.shape)
print(data[0,0:15])

# 3. create a single figure?
fig, ax = plt.subplots()

# 4. How to create color map with numpy table like array? 
im = ax.imshow(data, cmap='gist_earth')

# 5. How to add color map legend?    
fig.colorbar(im)

plt.show()
```




### example3
```python
import numpy as np
import matplotlib.pyplot as plt
np.random.seed(1)

# Generate data...

# 1. How to create custom x, y arrays ?
y_raw = np.random.randn(1000).cumsum() + 15
x_raw = np.linspace(0, 24, y_raw.size)

# 2. How to convert array to a table of 100 columns?  
# 3. How to get min value for each row of table? 
# collapse all columns to one value for each row 
x_pos = x_raw.reshape(-1, 100).min(axis=1)
# 4. How to get mean value for each row of table ? 
y_avg = y_raw.reshape(-1, 100).mean(axis=1)
# 5. How to get max-min value for each row of table? 
y_err = y_raw.reshape(-1, 100).ptp(axis=1)

bar_width = x_pos[1] - x_pos[0]

# Make a made up future prediction with a fake confidence
# 6. How to create two straight lines in x and y coords? 
x_pred = np.linspace(0, 30)
y_max_pred = y_avg[0] + y_err[0] + 2.3 * x_pred
y_min_pred = y_avg[0] - y_err[0] + 1.2 * x_pred

# Just so you don't have to guess at the colors...
barcolor, linecolor, fillcolor = 'wheat', 'salmon', 'lightblue'

# Now you're on your own!
fig, ax = plt.subplots()

# 7. How to create a line using x and y arrays? 
ax.plot(x_raw, y_raw, color=linecolor)

# 8. How to create barchart with error lines? 
ax.bar(x_pos, y_avg, width=bar_width, color=barcolor, yerr=y_err, 
       ecolor='gray', edgecolor='cyan')

# 9. How to create areaChart between two straight lines? 
ax.fill_between(x_pred, y_min_pred, y_max_pred, color=fillcolor)

# 10. How to set title, labels
ax.set(title='Future Projection of Attitudes', 
        ylabel='Snarkiness (snark units)', 
        xlabel='Minutes since class began')

plt.show()
```



### seed array figure barchart axisLine
```python
# Let's get our standard imports out of the way
from __future__ import print_function
import numpy as np
import matplotlib
matplotlib.use('nbagg')
import matplotlib.pyplot as plt

# set seed
np.random.seed(1)

# create arrays
x = np.arange(5)
y = np.random.randn(5)

# create 1row 2column figure
fig, axes = plt.subplots(ncols=2, figsize=plt.figaspect(1./2))

# create horizontal and vertical bars 
vert_bars = axes[0].bar(x, y, color='lightblue', align='center')
horiz_bars = axes[1].barh(x, y, color='lightblue', align='center')

# I'll also introduce axhline & axvline to draw a line all the way across the axes
# This can be a quick-n-easy way to draw an axis "spine".
axes[0].axhline(0, color='gray', linewidth=2)
axes[1].axvline(0, color='gray', linewidth=2)

plt.show()

##################

# create a single empty figure
fig, ax = plt.subplots()

# create a barchart 
vert_bars = ax.bar(x, y, color='lightblue', align='center')

# loop all to select certain bars and change them 
for bar in vert_bars:

# access x value with bar.xy[0], access y value with bar.xy[1]
    if bar.xy[0] < 2:
        bar.set(edgecolor='darkred', color='salmon', linewidth=3)

plt.show()

####################################### Create areaChart or fill_between y and 0

np.random.seed(1)

# 1. How to create a 100 random number and cumsum them? 
y = np.random.randn(100).cumsum()
# np.cumsum() 

# 2. How to create a 100 equal spaced numbers between 0 and 99?
x = np.linspace(0, 10, 100)
print("x head", x[0:5])

# 3. How to create a areaChart or fill_between chart between y value and 0?
fig, ax = plt.subplots()
ax.fill_between(x, y, color='lightblue')
plt.show()

####################################### create areaChart between two lines 

x = np.linspace(0, 10, 200)

# 4. How to create straight lines and curve line?
y1 = 2 * x + 1
y2 = 3 * x + 1.2
y_mean = 0.5 * x * np.cos(2*x) + 2.5 * x + 1.1

fig, ax = plt.subplots()

# 5. Plot the envelope with `fill_between`
ax.fill_between(x, y1, y2, color='yellow')

# 6. Plot the "centerCurveline" with `plot`
ax.plot(x, y_mean, color='black')

plt.show()


####################################### exercise  
# %load exercises/2.1-bar_and_fill_between.py
import numpy as np
import matplotlib.pyplot as plt
np.random.seed(1)

# Generate data...
y_raw = np.random.randn(1000).cumsum() + 15
x_raw = np.linspace(0, 24, y_raw.size)

# Get averages of every 100 samples...
x_pos = x_raw.reshape(-1, 100).min(axis=1)
y_avg = y_raw.reshape(-1, 100).mean(axis=1)
y_err = y_raw.reshape(-1, 100).ptp(axis=1)

bar_width = x_pos[1] - x_pos[0]

# Make a made up future prediction with a fake confidence
x_pred = np.linspace(0, 30)
y_max_pred = y_avg[0] + y_err[0] + 2.3 * x_pred
y_min_pred = y_avg[0] - y_err[0] + 1.2 * x_pred

# Just so you don't have to guess at the colors...
barcolor, linecolor, fillcolor = 'wheat', 'salmon', 'lightblue'

# Now you're on your own!


```



### array to multi dim table
=> How to turn a single array to multi-dim table?     
```python
y.shape = (4, 20, -1) # dimension, row, column
print(y.shape)
# print(y)
# print(y[0:3])
print(y[0:3, 11:15, 3:5])
y.shape = (2,2, -1)
# y.shape = (2,2,100)
print(y[0:2,0:2,0:3])
```
[Back](#part2)

### array to table
=> How to change an array to a table?    
```python
x.shape = (20, 5) # change single column to 20x5
print(x)
```
[Back](#part2)    



### create numpy array range    
=> How to create an array range 0-99
```python
x = np.arange(100)
print(x.shape)
print(x.size)
print(x.ndim)
```
[Back](#part2)    



### create numpy array
=> how to create a simple array
```python
a = np.array([1, 2, 3])
print(a.shape)
print(a.size)
print(a.ndim)
```
[Back](#part2)  


### numpy random table
=> How to create a random table?
```python
import numpy as np  
y = np.random.rand(5, 80)
print(y.shape)
print(y.size)
print(y.ndim)
y[0:5,0:8]
```
[Back](#part2)    




### numpy index     
=> How numpy array select by index    
```python
# Advanced slicing
print("First 5 rows\n", x[:5])
print("Row 18 to the end\n", x[18:])
print("Last 5 rows\n", x[-5:])
print("Reverse the rows\n", x[::-1])

# Fancy Indexing -- Note the use of a list, not tuple!
print(x[[1, 3, 8, 9, 2]])
```
[Back](#part2)    




### condition selection
=> How numpy array select on condition?    
```python
# Boolean Indexing
print(x[(x % 2) == 0])
```
[Back](#part2)    


 

### numpy array range intervals    
=> how to create array with specific range and intervals?    
```python
x = np.arange(-5, 5, 0.1)
y = np.arange(-8, 8, 0.25)
```
[Back](#part2)      




 



### row multiply column    
=> How to create a table by multiply a row array and a column array?    
- you know what the first row value is like
- you know what the first column value is like
- you want to the middle meat of the table to be row and column multiply
```python

x = np.arange(-5, 5, 0.1)
y = np.arange(-8, 8, 0.25)
print(x.shape)
print(y.shape)
x.shape = (-1,1)  # make it a multi-row but 1 column
y.shape = (1,-1) # make it a multi-column but 1 row
print(x.shape)
print(y.shape)
print((x*y).shape)

x,y = np.ogrid[-5:5:0.1, -8:8:0.25]
print(x.shape, y.shape)
z = x * y
print(z.shape)
```
[Back](#part2)      






### matplotlib version    
=> How to find out the version of matplotlib?
```python
import matplotlib
print(matplotlib.__version__)     
print(matplotlib.get_backend())    
```
[Back](#part2)      

 


### matplotlib inline    
=> How to plot graph inside jupyter cell?     
```python  
import matplotlib
print(matplotlib.__version__)
print(matplotlib.get_backend())

# Let's get our standard imports out of the way
from __future__ import print_function
import numpy as np
import matplotlib
matplotlib.use('nbagg') # or %matplotlib nbagg
import matplotlib.pyplot as plt

plt.show() # or not with %

```
[Back](#part2)       






### empty graph
=> How to create an empty graph    
```python
fig = plt.figure()
```
[Back](#part2)       





### empty graph double height
=> how to create a graph with double tall than wide
```python
# Twice as tall as it is wide:
fig = plt.figure(figsize=plt.figaspect(2.0))
```
[Back](#part2)       





### create axis title label
=> How to create a graph with axis, title and label?    
```python
fig = plt.figure()
ax = fig.add_subplot(111) # We'll explain the "111" later. Basically, 1 row and 1 column.
ax.set(xlim=[0.5, 4.5], ylim=[-2, 8], title='An Example Axes', ylabel='Y-Axis', xlabel='X-Axis')

###############################
fig = plt.figure()
ax = fig.add_subplot(111)
ax.set_xlim([0.5, 4.5])
ax.set_ylim([-2, 8])
ax.set_title('An Example Axes')
ax.set_ylabel('Y-Axis')
ax.set_xlabel('X-Axis')

```
[Back](#part2)        




### line scatterplot
=> create a graph with line plot and scatterplot
```python
fig = plt.figure()
ax = fig.add_subplot(111)
ax.plot([1, 2, 3, 4], [10, 20, 25, 30], color='lightblue', linewidth=3)
ax.scatter([0.3, 3.8, 1.2, 2.5], [11, 25, 9, 26], color='darkgreen', marker='^')
ax.set_xlim(0.5, 4.5)

##################### method 2
fig = plt.figure()
ax = fig.add_subplot(111)
plt.plot([1, 2, 3, 4], [10, 20, 25, 30], color='lightblue', linewidth=3)
plt.scatter([0.3, 3.8, 1.2, 2.5], [11, 25, 9, 26], color='darkgreen', marker='^')
plt.xlim(0.5, 4.5)

```
[Back](#part2)        




### multiple charts   
=> How to create multiple graphs on a chart?   
=> How to plot lines and scatterplot?
```python
fig, axes = plt.subplots(nrows=2, ncols=2)
axes[0,0].set(title='Upper Left')
axes[0,1].set(title='Upper Right')
axes[1,0].set(title='Lower Left')
axes[1,1].set(title='Lower Right')

# # To iterate over all items in a multidimensional numpy array, use the `flat` attribute
for ax in axes.flat:
    # Remove all xticks and yticks...
    ax.set(xticks=[], yticks=[])

################# a full example ##################
import matplotlib
print(matplotlib.__version__)
print(matplotlib.get_backend())

# method one
%matplotlib nbagg

import numpy as np
import matplotlib.pyplot as plt

# Try to reproduce the figure shown in images/exercise_1-1.png

# Our data...
x = np.linspace(0, 10, 100)
y1, y2, y3 = np.cos(x), np.cos(x + 1), np.cos(x + 2)
names = ['Signal 1', 'Signal 2', 'Signal 3']

names[1]

# Can you figure out what to do next to plot x vs y1, y2, and y3 on one figure?
fig, axes = plt.subplots(nrows=3, ncols=1)
axes[0].set(title=names[0])
axes[1].set(title=names[1])
axes[2].set(title=names[2])
axes[0].plot(y1, color='lightblue', linewidth=3)
axes[1].plot(y2, color='lightblue', linewidth=3)
axes[2].plot(y3, color='lightblue', linewidth=3)

```
[Back](#part2)        



### create a figure    
=> Three ways to create a figure or graph     
```python
fig = plt.figure() # a figure with a single axis
ax = fig.add_subplot(111) # a figure with a single axis

fig, ax = plt.subplots() # a figure with a single axis
```
[Back](#part2)     





### stats array 
=> How to use numpy statistics on numpy array?     
```python
np.mean(X)
np.std(X)
```





### histogram stock return
=> How to plot histogram out of a price series?    
```python
plt.hist(R, bins=20)
plt.xlabel('Return')
plt.ylabel('Frequency')
plt.legend(['MSFT Returns']);
```


### stock-series-return
=> How to calc return from a price series?    
- first element is 0/something is NaN
```python
R = X.pct_change()[1:] # avoid the NaN
print R.head()
R1 = X.pct_change()
print R1.head()
```
[Back](#quantopian)    



### plot stock series  
=> How to plot a stock series out of the stock dataframe?    
- a stock series has index and values 
- plt.plot(x, y) for coord (x,y)  
```python
X = data['price'] # close_price series of a stock dataframe
X.head()

plt.plot(X.index, X.values)
plt.ylabel('Price')
plt.legend(['MSFT']);
```
[Back](#quantopian)    


### stock daily
=> How to access a stock daily data?    
- set symbol name
- set start and end date
- set fields
- return dataframe 
```python
data = get_pricing('MSFT', start_date='2012-1-1', end_date='2015-6-1') 
data = get_pricing('TSLA', start_date='2012-1-1', end_date='', fields = ['open_price', 'close_price'])
```
[Back](#quantopian)    


## plotting   

[How to plot with a single np array?](#plot-array)    
[How to plot 2 arrays with labels and legend?](#2array-labels-legend)    

### 2array labels legend    
=> How to plot 2 arrays with labels and legend?    
```python
import numpy as np
import matplotlib.pyplot as plt

X = np.random.normal(0, 1, 100)
X2 = np.random.normal(0, 1, 100)

plt.plot(X);
plt.plot(X2);
plt.xlabel('Time') # The data we generated is unitless, but don't forget units in general.
plt.ylabel('Returns')
plt.legend(['X', 'X2']);
```
[Back](#plotting)    



### plot array   
=> How to plot with a single np array?    
```python
# This is a plotting library for pretty pictures.
import matplotlib.pyplot as plt

# Sample 100 points with a mean of 0 and an std of 1. This is a standard normal distribution.
X = np.random.normal(0, 1, 100)
X[0:5]
len(X)
type(X)

%matplotlib inline
plt.plot(X)
```
[Back](#plotting)    






### row bind dataframe 
=> How to row-bind dataframe?    
```python
df_new = pd.concat([df_a, df_b])
df_new
```


### create dataframe    
=> How to create a small dataframe?     
```python
raw_data = {
        'subject_id': ['4', '5', '6', '7', '8'],
        'first_name': ['Billy', 'Brian', 'Bran', 'Bryce', 'Betty'], 
        'last_name': ['Bonder', 'Black', 'Balwner', 'Brice', 'Btisan']}
df_b = pd.DataFrame(raw_data, columns = ['subject_id', 'first_name', 'last_name'])
df_b
```
[Back](#m2-vs-stocks)     


### random nparray type    
=> How to create a random array and test type?    
```python
import numpy as np
# Sample 100 points with a mean of 0 and an std of 1. This is a standard normal distribution.
X = np.random.normal(0, 1, 100)
X[0:5]
len(X)
type(X)
```
[Back](#m2-vs-stocks)     

### string methods
=> How to use string methods in pandas?    
```python
orders = pd.read_table('chiporder.tsv')
orders.head()

# string methods for pandas Series are accessed via 'str'
orders.item_name.str.upper().head()

# string method 'contains' checks for a substring and returns a boolean Series
orders.item_name.str.contains('Chicken').head()

# use the boolean Series to filter the DataFrame
orders[orders.item_name.str.contains('Chicken')].head()

# string methods can be chained together
orders.choice_description.str.replace('[', '').str.replace(']', '').head()

# many pandas string methods support regular expressions (regex)
orders.choice_description.str.replace('[\[\]]', '').head()
```
[Back](#m2-vs-stocks)     



### axis row column
=> How to refer to rows and columns with axis=0,1,'index','column'?    
- axis = 0 equal to axis = 'index', collapse values vertically or row by row
- axis = 1 equal to axis = 'column', collapse values horizontally or column by column       
```python   
# calculate the mean of each numeric column
drinks.mean()

# or equivalently, specify the axis explicitly, collapse rows into one 
drinks.mean(axis=0)

# 'index' is an alias for axis 0
drinks.mean(axis='index')

# calculate the mean of each row, collapse columns into one 
drinks.mean(axis=1).head()

# 'columns' is an alias for axis 1
drinks.mean(axis='columns').head()
```
[Back](#m2-vs-stocks)     




### drop inplace     
=> How to understand use of `inplace=True` in drop columns and rows of a dataframe?    
- inplace = True: set it permanently 

```python
import pandas as pd
ufo = pd.read_csv('ufo.csv')

# drop rows temporarily
print ufo.drop(2, axis=0).head() # remove the 3rd row
print ufo.head()

# drop columns temporarily
print ufo.drop('Time', axis=1).columns
print ufo.columns

# drop permanently
ufo.drop([0,1,4], inplace=True, axis=0) # remove the first,second,fifth row
print ufo.head()
```
[Back](#m2-vs-stocks)     



### describe dataframe    
=> How to describe only numeric, all, or specific columns of a dataframe?    
```python
# describe all of the numeric columns
drinks.describe()

# pass the string 'all' to describe all columns including strings and others 
drinks.describe(include='all')

# pass a list of data types to only describe certain types
drinks.describe(include=['object', 'float64'])

# pass a list even if you only want to describe a single data type
drinks.describe(include=['object'])
```
[Back](#m2-vs-stocks)     



### numeric columns    
=> How to drop all non-numeric columns or only keep numeric columns of a dataframe?    
```python
# read a dataset of alcohol consumption into a DataFrame, and check the data types
import pandas as pd
drinks = pd.read_csv('drinks.csv')
drinks.dtypes

# only include numeric columns in the DataFrame
import numpy as np
drinks.select_dtypes(include=[np.number]).dtypes
```
[Back](#m2-vs-stocks)     



### iterate dataframe    
=> How to iterate a dataframe by rows?    
```python
# various methods are available to iterate through a DataFrame
for index, row in ufo.iterrows():
    print(index, row.City, row.State)
```
[Back](#m2-vs-stocks)     



### read specific rows    
=> How to only read certain rows of dataframe?     
- when dealing with huge dataset  
```python
ufo = pd.read_csv('http://bit.ly/uforeports', nrows=3)
ufo
```
[Back](#m2-vs-stocks)     


### read specific columns    
=> How to read csv with only specific columns?    
- when dealing with huge dataset   
```python
ufo = pd.read_csv('http://bit.ly/uforeports')
ufo.columns
ufo = pd.read_csv('http://bit.ly/uforeports', usecols=['City', 'State'])
ufo = pd.read_csv('http://bit.ly/uforeports', usecols=[0, 4])
ufo.columns
```
[Back](#m2-vs-stocks)     


### more filters
=> How to filter by multiple conditions on columns?    
```python
# use the '|' operator to specify that a row can match any of the three criteria
movies[(movies.genre == 'Crime') | (movies.genre == 'Drama') | (movies.genre == 'Action')].head(10)

# or equivalently, use the 'isin' method
movies[movies.genre.isin(['Crime', 'Drama', 'Action'])].head(10)
```
[Back](#m2-vs-stocks)     


### or and 
```python
True or False
False or False
True and True
True and False
data[(data.duration' > 200) & (data.type == 'genre')] # and
data[(data.duration' > 200) | (data.type == 'genre')] # pipe

```
[Back](#m2-vs-stocks)     


### filter rows    
=> How to filter rows of a dataframe?    
```python
is_long_series = pd.Series(is_long_list)
data[is_long_series]
data[data.duration > 200]
data[data.duration > 200].genre
data[data.duration > 200]['genre']
# better solution: first row filter and then column selection 
data.loc(data.duration > 200, 'genre')
```
[Back](#m2-vs-stocks)     


### list to series    
=> How to convert a list to a series?    
```python
is_long_series = pd.Series(is_long_list)
```
[Back](#m2-vs-stocks)     

### length list dataframe     
=> How to check length of a list?    
```python
len(list)
len(dataframe)
```
[Back](#m2-vs-stocks)     


### fill list    
=> How to fill a list using for in loop and append?    
```python
# create a list in which each element refers to a DataFrame row: True if the row satisfies the condition, False otherwise
booleans = []
for length in movies.duration:
    if length >= 200:
        booleans.append(True)
    else:
        booleans.append(False)

```
[Back](#m2-vs-stocks)     

### sort dataframe    
```python
import pandas as pd
movies = pd.read_csv('imdb_1000.csv')
movies.title.sort_values()
movies['title'].sort_values(ascending=False)
movies.sort_values('title')
movies.sort_values('title', ascending=False)
movies.sort_values(['content_rating', 'duration'], ascending=False)
```
[Back](#m2-vs-stocks)     


### structure dataframe 
```python
print ufo.ndim  # dimension
print ufo.size  # rows * columns
print ufo.shape # (rows, columns)
print ufo.dtypes # columns types 
```
[Back](#m2-vs-stocks)     


### remove rows  
=> How to remove rows of a dataframe?    
- row name -> index or labels 
- use list to include row names 
- axis = 0 is default
```python
import pandas as pd
ufo = pd.read_csv('ufo.csv')
ufo.drop(2, inplace=True, axis=0) # remove the 3rd row
ufo.drop([0,1,4], inplace=True, axis=0) # remove the first,second,fifth row
```
[Back](#m2-vs-stocks)     



### remove columns
=> How to remove columns of a dataframe?    
- axis 0 -> rows, axis 1 -> columns    
- inplace = True -> convension
```python
import pandas as pd
ufo = pd.read_csv('ufo.csv')
ufo.drop('Colors reported', inplace=True, axis=1)
ufo.drop(['State', 'City'], inplace=True, axis=1)
```
[Back](#m2-vs-stocks)     



### rename columns    
=> How to rename columns of a dataframe?     
```python
import pandas as pd
ufo = pd.read_csv('ufo.csv')
ufo.head()

# rename two of the columns by using the 'rename' method
ufo.rename(columns={'Colors Reported':'Colors_Reported', 'Shape Reported':'Shape_Reported'}, inplace=True)
ufo.columns # check column names 

# replace all of the column names by overwriting the 'columns' attribute
ufo_cols = ['city', 'colors reported', 'shape reported', 'state', 'time']
ufo.columns = ufo_cols    
ufo.columns   

# replace the column names during the file reading process by using the 'names' parameter
ufo = pd.read_csv('http://bit.ly/uforeports', header=0, names=ufo_cols)
ufo.columns
# Explicitly pass header=0 to be able to replace existing names

# replace all spaces with underscores in the column names by using the 'str.replace' method
ufo.columns = ufo.columns.str.replace(' ', '_')
ufo.columns
```
[video](https://youtu.be/A5mwmidZnug)    
[Back](#m2-vs-stocks)     



### install update libraries    
=> How to install and update libraries, diff versions?     
```python
python -m pip install SomePackage    
python -m pip install SomePackage==1.0.4    # specific version
python -m pip install "SomePackage>=1.0.4"  # minimum version
# to update is to install again, or the following code 
python -m pip install --upgrade SomePackage
```
[Back](#m2-vs-stocks)    

### check api
=> How to check a function's api?    
- put cursor inside ()
- press shift + tab 1-4 times 
```python
type(data)
```
[Back](#m2-vs-stocks)    


### dtypes
=> How to get the types of all columns of a dataframe?    
- float64
- int64
- object => just meaning strings   
```python
data.dtypes
```
[Back](#m2-vs-stocks)    

### func method attribute
=> How to understand function, method and attributes to a dataframe or series?     
```python 
data.dtypes # dataframe's attributes
data.shape  # dataframe's attributes
data.head() # method
data.describe() # method
type(data) # function 
```
[Back](#m2-vs-stocks)    


### data summary
=> How to check basic summary of a dataframe?    
```python
import pandas as pd
data = pd.read_csv('imdb_1000.csv')
data.describe()
```
[Back](#m2-vs-stocks)    


### get type
=> How to know an object's type?     
```python
type(data1) # dataframe
type(data1['City'])  # series
```
[Back](#m2-vs-stocks)    



### dataframe series
=> What is a dataframe and a pandas series?     
- dataframe is a table like dataset  
- a series is a column of this dataframe 
[Back](#m2-vs-stocks)    




### jupyter
=> How to use jupyter notebook?    
- `esc` for command mode   
- `m` for markdown  
- `y` for coding   
- `o` toggle output of selected cell  
- `a` insert a cell above
- `b` insert a cell below
- up down arrow to move between cells 
- `space` and `shift space` to move to top and bottom of page 
- `enter` to step into edit mode
[Back](#m2-vs-stocks)    


### read dirty comment file    
=> How to read dirty file ignoring pre and post comment?   
- first 2 lines are comments 
- last 2 lines are comments too
```python
import pandas as pd
pd.read_table('drinks_topbottom.csv', sep=',', skiprows=2, skip_footer=2)
```
[Back](#m2-vs-stocks)    



### read csv   
=> How to read a simple csv file with read_table?   
```python
import pandas as pd  
data1 = pd.read_table('drinks.csv', sep=',')
data2 = pd.read_csv('drinks.csv')
```
[Back](#m2-vs-stocks)    

### read dirty file    
=> How to read dirty file? 
- sep by |
- no header
- add custom colnames 
```python
import pandas as pd
user_cols=['user_id', 'age', 'gender', 'occupation', 'zip_code']
data1=pd.read_table("u.user.txt", header=None, sep='|', names=user_cols)
```
[Back](#m2-vs-stocks)    


### read tsv   
=> How to read a tsv file? 
```python
import pandas as pd
# default is tsv format
data = pd.read_table("chipotle.tsv")
```
[Back](#m2-vs-stocks)    

### stock print nicely    
=> How to print out stock data info nicely?     
```python 
print dailydata.to_html()
```
[demo](https://uqer.io/labs/notebooks/get%20monthly%20and%20weekly%20data%20.nb)     
[Back](#m2-vs-stocks)    


### daily weekly monthly data
=> How to get daily, weekly, monthly stock data?  
```python
dailydata = DataAPI.MktEqudAdjGet(secID = '600298.XSHG' ,beginDate=u"20160401",endDate=u"",field=u"",pandas="1")
weeklydata = DataAPI.MktEquwAdjGet(secID = '600298.XSHG' ,beginDate=u"20160401",endDate=u"",field=u"",pandas="1")
monthlydata = DataAPI.MktEqumAdjGet(secID = '600298.XSHG' ,beginDate=u"20160401",endDate=u"",field=u"",pandas="1")
```
[demo](https://uqer.io/labs/notebooks/get%20monthly%20and%20weekly%20data%20.nb)    
[Back](#m2-vs-stocks)    


### make func    
=> How to turn codes into a function to easily change a parameter?    
```python   
def get_returnMean(N):   #传入的是持有的天数
    buydata = pd.DataFrame()
    buydata['secID'] = liangrongdata['secID']
    buydata['buydate'] = map(lambda x: date[date.index(x)+1], liangrongdata['intoDate'].values.tolist())  #纳入标的的第二天的交易日
    buydata['selldate'] = map(lambda x: date[date.index(x)+1+N], liangrongdata['intoDate'].values.tolist())  #持有N天后的交易日
    buydata['buyprice'] = np.zeros(len(buydata))
    buydata['sellprice'] = np.zeros(len(buydata))
    for i in range(len(buydata)):
        buydata.iat[i,3] = DataAPI.MktEqudAdjGet(tradeDate=buydata.iat[i,1],secID=buydata.iat[i,0],field='closePrice').iat[0,0]
        buydata.iat[i,4] = DataAPI.MktEqudAdjGet(tradeDate=buydata.iat[i,2],secID=buydata.iat[i,0],field='closePrice').iat[0,0]
    buydata['return'] = buydata['sellprice']/buydata['buyprice']-1
    return buydata['return']  #返回收益的序列 
```
[video](https://youtu.be/t9BjCFywtY0)    
[Back](#m2-vs-stocks)    


### statistics    
=> How to do basic statistics like `mean()`?    
```python
buydata['return'].mean()    
```
[Back](#m2-vs-stocks)    



### fill up column    
=> How to fill up columns with 0s with `len(), range(), .iat()`?    
```python
for i in range(len(buydata)):
    buydata.iat[i,3] = DataAPI.MktEqudAdjGet(tradeDate=buydata.iat[i,1],secID=buydata.iat[i,0],field='closePrice').iat[0,0]  #获取买入时的前复权收盘价
    buydata.iat[i,4] = DataAPI.MktEqudAdjGet(tradeDate=buydata.iat[i,2],secID=buydata.iat[i,0],field='closePrice').iat[0,0]  #获取卖出时的前复权收盘价
    
# create a list in which each element refers to a DataFrame row: True if the row satisfies the condition, False otherwise
booleans = []
for length in movies.duration:
    if length >= 200:
        booleans.append(True)
    else:
        booleans.append(False)    
```
[video](https://youtu.be/2ttOzZx-MgM )    
[demo](https://uqer.io/labs/notebooks/unpaid%20api%20and%20build%20dataframe.nb)    
[Back](#m2-vs-stocks)    


### for in range    
=> How to use for in loop with range?    
```python
for i in range(len(buydata)): 
```
[demo](https://uqer.io/labs/notebooks/unpaid%20api%20and%20build%20dataframe.nb)    
[Back](#m2-vs-stocks)    



### dataframe from scratch    
=> How to create a dataframe from scatch?    
```python
import pandas as pd
import numpy as np

buydata = pd.DataFrame()  
buydata['secID'] = liangrongdata['secID']   
buydata['buydate'] = map(lambda x: date[date.index(x)+1], liangrongdata['intoDate'].values.tolist())  
buydata['selldate'] = map(lambda x: date[date.index(x)+11], liangrongdata['intoDate'].values.tolist())  #持有十天后的交易日
buydata['buyprice'] = np.zeros(len(buydata)) 
buydata['sellprice'] = np.zeros(len(buydata))
```
[video](https://youtu.be/pH7Us_xOcgU)    
[demo](https://uqer.io/labs/notebooks/unpaid%20api%20and%20build%20dataframe.nb)    
[Back](#m2-vs-stocks)    


### create column     
=> How to tranform or create a new column of a dataframe?    
- must use [] method not . method    
```python    
ufo['location'] = ufo.City + ", " + ufo.State
buydata['secID'] = liangrongdata['secID']      
buydata['buydate'] = map(lambda x: date[date.index(x)+1], liangrongdata['intoDate'].values.tolist())     
buydata['buyprice'] = np.zeros(len(buydata))    
for i in range(len(buydata)):   
    buydata.iat[i,4] = DataAPI.MktEqudAdjGet(tradeDate=buydata.iat[i,2],secID=buydata.iat[i,0],field='closePrice').iat[0,0]
```


### create empty dataframe    
=> How to create an empty dataframe?    
```python 
buydata = pd.DataFrame()  
```
[demo](https://uqer.io/labs/notebooks/unpaid%20api%20and%20build%20dataframe.nb)    
[Back](#m2-vs-stocks)    


### unpaid API    
=> How to search and access unpaid API?    
- there is a free to try option 
- try english and chinese names to search and scroll  

[video](https://youtu.be/2liaQwRP0Qs)    
[Back](#m2-vs-stocks)    




### first n rows    
=> How to read first/last 10 rows of a dataframe?    
```python
liangrongdata.head(10)  #前十个数据
buydata.tail(10) # last 10
data[0:10]
data[-10:-1]
```
[Back](#m2-vs-stocks)    


### column to list   
=> 3 ways to turn a column of a dataframe to a list 
```python
stklist.tolist()
stklist.values.tolist()
stklist.unique().tolist()
```
[video](https://youtu.be/LxeSVlmpbRQ)    
[demo](https://uqer.io/labs/notebooks/stocks%20borrow%20to%20sell.nb)    
[Back](#m2-vs-stocks)     


### borrow sell    
=> How to get all stock names which can be borrowed to sell?    
```python
stklist = DataAPI.FstDetailGet(secID=set_universe('A'),beginDate=u"20160701").secID.unique().tolist()    
```
- access a column of a dataframe    
- filter for only unique names/values  
- turn the column to a list     

[video](https://youtu.be/x41umRPEulQ)    
[demo](https://uqer.io/labs/notebooks/stocks%20borrow%20to%20sell.nb)    
[Back](#m2-vs-stocks)     


### tranform date string
=> How to convert "2016-08-12" to "20160812"?    
```python
date = map(lambda x: x[0:4]+x[5:7]+x[8:10], data['calendarDate'].values.tolist())   
```
[video](https://youtu.be/SBeO6uurvU0)      
[demo](https://uqer.io/labs/notebooks/date%20string%20without%20space.nb)    
[Back](#m2-vs-stocks)    


### filter out rows
=> How to filter out rows using a column?     
```python
data = data[data['isOpen'] == 1]
```
[video](https://youtu.be/SBeO6uurvU0 )    
[Back](#m2-vs-stocks)   


### trading date shanghai
=> How to access all trading calendar date of ShangHai market?    
```python
data = DataAPI.TradeCalGet(exchangeCD=u"XSHG",beginDate='20070101',endDate='20160731',field=['calendarDate','isOpen'])
# files = a list above; 
```
[video](https://youtu.be/jtb69Y-2Nmg)    
[demo](https://uqer.io/labs/notebooks/trading%20date.nb)    
[Back](#m2-vs-stocks)   


### import lib    
=> How to import libraries with diff options    
```python
import numpy as np # import the whole lib
import pandas as pd 
from matplotlib import pylab # import a func of a lib
import matplotlib.pyplot as plt # import a func of a lib and give it a short name
from matplotlib.pyplot import * # import a lib's sub lib and import everything inside the sub lib
matplotlib.style.use('ggplot') # set plot style  
import seaborn as sns 

from CAL.PyCAL import *
font.set_size(22)  # set font size
```
[video](https://youtu.be/hZ8XWL_YO7g)     
[demo](https://uqer.io/labs/notebooks/import%20library.nb)    
[Back](#m2-vs-stocks)   


### save csv
=> How to save dataframe to csv file?     
```pyhton
data2016.to_csv("AB2016.csv", encoding="GBK") 
```
[video](https://youtu.be/OUC58dv2uqs)      
[demo](https://uqer.io/labs/notebooks/access%20column%20and%20save%20to%20csv.nb)    
[Back](#m2-vs-stocks)   


### access column    
=> How to access a column from a dataframe?     
- [] method is universally working on all kinds of names 
- . method only works for well-behaved column names
```python
# [] works for all situations 
data2006["ticker"] # column name "ticker"
data2006["sec short name"] # data2006.sec_short_name won't work   
data2006["head"] # data2006.head won't get you the 'head' column, as they are syntax terms 
data2006.ticker # . method works for more ideal and regular column names 
```
[video](https://youtu.be/UrLETCTByNo)    
[demo](https://uqer.io/labs/notebooks/access%20column%20and%20save%20to%20csv.nb)     
[Back](#m2-vs-stocks)    


### M2 10years plot    
=> How to plot 10-year M2 change?     
- access M2 data with cash value     
- plot it with seaborn    

```python
data = DataAPI.ChinaDataMoneyStatisticsGet(indicID=u"M100000005",indicName=u"",beginDate=u"20060101",endDate=u"20160901",field=u"indicID,indicName,periodDate,dataValue,unit",pandas="1")

data

import seaborn
data.plot(x='periodDate', y='dataValue',title=u'M2-in-10-years',figsize=(14,6))
```

[video](https://youtu.be/XGQbOtntqds)
[demo](https://uqer.io/labs/notebooks/M2-plot.nb)
[Back](#m2-vs-stocks)    


### search use DataAPI
=> How to search and use DataAPI?     
- Where to find detail of DataAPI doc?
- How to apply a group of fields?
- A useful dataAPI to remember    

[video](https://youtu.be/JaTep5fvaNM)    
[demo](https://uqer.io/labs/notebooks/DataAPI%20Learning.nb)    
[Back](#m2-vs-stocks)    

