# iPython-by-exmaples

## **Table of Content**

## M2 vs Stocks

[How to convert "2016-08-12" to "20160812"?](#transform-date-string)    
[How to filter out rows using a column?](#filter-out-rows)    
[How to access all trading calendar date of ShangHai market?](#trading-date-shanghai)    
[How to import libraries](#import-lib)    
[How to save dataframe to csv file?](#save-csv)    
[How to access a column of a dataframe?](#access-column)    
[How to plot M2-10-year change?](#m2-10years-plot)    
[How to search and use DataAPI?](#search-use-dataapi)    


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

