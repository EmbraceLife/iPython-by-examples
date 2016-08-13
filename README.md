# iPython-by-exmaples

## **Table of Content**

## M2 vs Stocks

[How to import libraries](#import-lib)    
[How to save dataframe to csv file?](#save-csv)    
[How to access a column of a dataframe?](#access-column)    
[How to plot M2-10-year change?](#m2-10years-plot)    
[How to search and use DataAPI?](#search-use-dataapi)    



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
[video](uploading)     
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
```python
tickers2006 = data2006["ticker"] # column name "ticker"
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

