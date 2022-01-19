### Multiplicative decomposition[](https://otexts.com/fpp2/classical-decomposition.html#multiplicative-decomposition)

A classical multiplicative decomposition is similar, except that the subtractions are replaced by divisions.

Step 1

If m

is an even number, compute the trend-cycle component ^Tt using a 2×m-MA. If m is an odd number, compute the trend-cycle component ^Tt using an m

-MA.

Step 2

Calculate the detrended series: yt/^Tt

.

Step 3

To estimate the seasonal component for each season, simply average the detrended values for that season. For example, with monthly data, the seasonal index for March is the average of all the detrended March values in the data. These seasonal indexes are then adjusted to ensure that they add to m

. The seasonal component is obtained by stringing together these monthly indexes, and then replicating the sequence for each year of data. This gives ^St

.

Step 4

The remainder component is calculated by dividing out the estimated seasonal and trend-cycle components: ^Rt=yt/(^Tt^St)

.

Figure [6.8](https://otexts.com/fpp2/classical-decomposition.html#fig:classical-elecequip) shows a classical decomposition of the electrical equipment index. Compare this decomposition with that shown in Figure [6.1](https://otexts.com/fpp2/components.html#fig:elecequip-trend). The run of remainder values below 1 in 2009 suggests that there is some “leakage” of the trend-cycle component into the remainder component. The trend-cycle estimate has over-smoothed the drop in the data, and the corresponding remainder values have been affected by the poor trend-cycle estimate.

```
elecequip %>% decompose(type="multiplicative") %>%
  autoplot() + xlab("Year") +
  ggtitle("Classical multiplicative decomposition
    of electrical equipment index")
```

![A classical multiplicative decomposition of the new orders index for electrical equipment.](https://otexts.com/fpp2/fpp_files/figure-html/classical-elecequip-1.png)

Figure 6.8: A classical multiplicative decomposition of the new orders index for electrical equipment.

### Comments on classical decomposition[](https://otexts.com/fpp2/classical-decomposition.html#comments-on-classical-decomposition)

While classical decomposition is still widely used, it is not recommended, as there are now several much better methods. Some of the problems with classical decomposition are summarised below.

-   The estimate of the trend-cycle is unavailable for the first few and last few observations. For example, if m=12
    

-   , there is no trend-cycle estimate for the first six or the last six observations. Consequently, there is also no estimate of the remainder component for the same time periods.
    
-   The trend-cycle estimate tends to over-smooth rapid rises and falls in the data (as seen in the above example).
    
-   Classical decomposition methods assume that the seasonal component repeats from year to year. For many series, this is a reasonable assumption, but for some longer series it is not. For example, electricity demand patterns have changed over time as air conditioning has become more widespread. Specifically, in many locations, the seasonal usage pattern from several decades ago had its maximum demand in winter (due to heating), while the current seasonal pattern has its maximum demand in summer (due to air conditioning). The classical decomposition methods are unable to capture these seasonal changes over time.
    
-   Occasionally, the values of the time series in a small number of periods may be particularly unusual. For example, the monthly air passenger traffic may be affected by an industrial dispute, making the traffic during the dispute different from usual. The classical method is not robust to these kinds of unusual values.