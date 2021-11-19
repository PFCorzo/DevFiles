# Resampling with Pandas 

Pandas `dataframe.resample()` function is primarily used for time series data.  
A time series is a series of data points indexed (or listed or graphed) in time order. Most commonly, a time series is a sequence taken at successive equally spaced points in time. It is a Convenience method for frequency conversion and resampling of time series. Object must have a datetime-like index (DatetimeIndex, PeriodIndex, or TimedeltaIndex), or pass datetime-like values to the on or level keyword.

Resampling generates a unique sampling distribution on the basis of the actual data. We can apply various frequency to resample our time series data. This is a very important technique in the field of analytics.  
Most commonly used time series frequency are –  
**W :** weekly frequency  
**M :** month end frequency  
**SM :** semi-month end frequency (15th and end of month)  
**Q :** quarter end frequency

There are many other types of time series frequency available. Let’s see how to apply these time series frequency on data and resample it.

## Syntax and Parameters

**Syntax :** DataFrame.resample(rule, how=None, axis=0, fill_method=None, closed=None, label=None, convention=’start’, kind=None, loffset=None, limit=None, base=0, on=None, level=None)

 **rule :** the offset string or object representing target conversion  
 **axis :** int, optional, default 0  
 **closed :** {‘right’, ‘left’}  
 **label :** {‘right’, ‘left’}  
 **convention :** For PeriodIndex only, controls whether to use the start or end of rule  
 **loffset :** Adjust the resampled time labels  
 **base :** For frequencies that evenly subdivide 1 day, the “origin” of the aggregated intervals. For example, for ‘5min’ frequency, base could range from 0 through 4. Defaults to 0.  
 **on :** For a DataFrame, column to use instead of index for resampling. Column must be datetime-like.  
 **level :** For a MultiIndex, level (name or number) to use for resampling. Level must be datetime-like.