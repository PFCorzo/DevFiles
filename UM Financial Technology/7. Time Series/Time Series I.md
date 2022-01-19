# Intro to Machine Learning and Time Series Analysis 

[[Deep-Machine Learning]] is a programming approach allowing applications to learn from the [[Inputs]] and make adjustments based on their [[Output]]. It is a devoloping [[Statistical Models]] that can make predictions or deciscions on new data automatically. 

Machine learning is used for the following predictions: 
* Loan eligibility, foreclosure rates, and fraud.
* Disease, diagnosis, and prognosis 
* Consumer segmentation and clustering 
* Presidential election results 
* Natural disasters and planetary climate impacts 

## Machine Learning Models 
Models for machine learning are provided in [[Libraries]] (HvPlot, Plotly, stuff like that) and all machine learning [[Pipelines]] follow the following [[Paradigm]]: (1)create a statistcal model, (2)[[Fit]] to feed data into them, and (3)let the machine output [[Predict]] the outcome. 

[[Intelligent Algorithms]] (AI) are ones that respond to data such that the algorithm gets better. It effectively "evolves". The deciscion is no longer deterministic given the event. 
AI are algorithms that use data to modify its behavior. They differ in that they can change their behavior as they run. 

### Types of Machine Learning 
There are three types of learning: Supervised learning and Unsupervised learning. 

**[[Supervised Learning]]** is where the system takes data and make predictable outcomes based on the math its doing to that data. Often times, it is [[Classification]] questions and [[Regression]] questions. 

**[[Unsupervised Learning]]** is where you feed the machine data and it starts genralizing an outcome by reducing the complexity of the data, or clustering the data. 

**[[Reinforcemnent Learning]]** 

## Time Series Basics 

A time series is a series of data points indexed (or listed or graphed) in time order.
Working with time series data requires data to be sliced and diced at various time frequencies in order to analyze data points as a time series. i.e., day/week/month/year. 

Pandas offers the best function to slice and dice data and is usually done in the following order. 

Example:

### Get information of the CSV

If the file is in a CSV assign a variable as df to read the CSV 
```
df = pd.read_csv(Insert the path to the csv)
```
View the head of the file ```df.head()``` and use ```df.info()``` to view more information. 

Let's see an example of Pandas reading a CSV file and asking for its information.

![[Pasted image 20211117104240.png]]

In the first line of information, you will notice that the index is a range that stems from 0 to 335. You will also notice that under data type(**Dtype**) the "datetime" column is marked as an object.

The problem is that when you use [[%matplotlib]] to plot the graph, you will get shown a line graph that it's x-axis is in the range of 0-335 rather than dates. 

![[Pasted image 20211117110109.png]]

To correct this error use Pandas to parse the dates and alter the index column. 

### Parse dates and alter index column. 
If you get information that was giving you a range index, but was giving you a  Range[[Index]],you will need to parse the dates and create a datetime index. 
If the file is in a CSV: assign a variable as df to read the CSV, set parse dates as true, and create a index column. 
```
df = pd.read_csv(Path, parse_date=true, index_col="datetime")
```

![[Pasted image 20211117104300.png]]

**NOW**, In the first line of information, you will notice that the index is in datetime that goes from 1980 to 2007. You will also notice that the "datetime" column has dissapeared. 

Now when you use [[%matplotlib]] to plot the graph, you will get shown a line graph that it's x-axis is in the range of 1980 - 2007 rather than dates. 

![[Pasted image 20211117122130.png]]

Now you can use df.loc to get the data for a specific year as well. 

### df.loc 
Since the first year is 1980, set a variable where ``` first_year = df.loc['1980']``` and plot the newly created variable by setting the variable prior to the column you want to retrieve the data from: ```first_year.liquor_sales.plot()```. Since you selected ['1980'] you will get the data from the entire year. 

You can get more specific by creating another variable like:
* specific_date1 = df.loc['1982-10']
	Which will give you the ['10'] month in the year ['1982'].
* specific_date2 = df.loc['October 1, 1982'] 
	Which will give you the 1st of October in the year 1982 
* specific_date3 = df.loc['1982-Oct-1']
	Which will also give you the 1st of October in the year 1982 
* two_year_period = df.loc["1985":"1986"]
	Which will give you 
	
### Resampling 
Pandas [[Resample]] is a convenience method for frequency conversion and resampling of time series data. 
In simpler words, you can arrange the time series data in patterns like monthly, weekly, daily, etc.,
**It works on the condition that objects have a datetime index.** 

```weekly_resampled_data = df.resample('W').mean()```
Here a variable was created ```weekly_resampled_data =``` that hold the data frame ```df.``` that we created out of the CSV file earlier, and told it to resample by week ```resample('W').mean()```
		                                                                                   

## Time Series Decomposition 

[[Time Series Decomposition]] is the seperation of time series into useful and less useful component. The useful components can be used to observe patterns and make predictions. There are three types of decompositions: 
* [[Classical decomposition]]
* [[Additive decomposition]]
* [[Multiplicative decomposition]]

There are four parameters: 
**Level**: What is the average value of the series? 
**Trend**: Is there an overall direction of movement? 
**Periodicity**: Do patterns occur in cycles?
**Residual**: How much noise exist in data? 

You would basically be getting the data for Level, Trend, Periodicty, and the data that would be left offer will be the residual. In order to effectively decompose a time series you will need to have the following dependencies: 
* Pandas 
* Pathlib
* [[statsmodels.tsa.seasonal]] import seasonal decompose 
* **Objects have a date time index.**

Example: 

```decomposed = seasonal_decompose(df['liquor_sales'], model='multiplicative')```
Here a variable was created ```decomposed =``` and the ```seasonal_decompose(``` function was enabled to modify the dataframe ```df``` that was already targeting the liqour sales ```['liqour_sales'],``` the seasonal decompose is then specified to be a multiplicative model ```model ='multiplicative')```

The result is the following: 

![[Pasted image 20211117174511.png]]
*Where Observed = Level, Trend = Trend, Seasonal = Periodicity, Residual = Residual*

## Exponential Weighted Moving Average 


































