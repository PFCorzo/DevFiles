### Additive decomposition[](https://otexts.com/fpp2/classical-decomposition.html#additive-decomposition)

Step 1

If m

is an even number, compute the trend-cycle component ^Tt using a 2×m-MA. If m is an odd number, compute the trend-cycle component ^Tt using an m

-MA.

Step 2

Calculate the detrended series: yt−^Tt

.

Step 3

To estimate the seasonal component for each season, simply average the detrended values for that season. For example, with monthly data, the seasonal component for March is the average of all the detrended March values in the data. These seasonal component values are then adjusted to ensure that they add to zero. The seasonal component is obtained by stringing together these monthly values, and then replicating the sequence for each year of data. This gives ^St

.

Step 4

The remainder component is calculated by subtracting the estimated seasonal and trend-cycle components: ^Rt=yt−^Tt−^St

.