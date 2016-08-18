# iPython-by-exmaples

## **Table of Content**

## M2 vs Stocks

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
[How to read first 10 rows of a dataframe?](#first-n-rows)    
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

### read dirty comment file    
=> How to read dirty file ignoring pre and post comment?   
- first 2 lines are comments 
- last 2 lines are comments too
```python
import pandas as pd
pd.read_table('drinks_topbottom.csv', sep=',', skiprows=2, skip_footer=2)
```

### read csv   
=> How to read a simple csv file with read_table?   
```python
import pandas as pd  
data3=pd.read_table('drinks.csv', sep=',')
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
=> How to tranform a column of a dataframe?    
```python    
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
=> How to read first 10 rows of a dataframe?    
```python
liangrongdata.head(10)  #前十个数据
buydata.tail(10) # last 10
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

