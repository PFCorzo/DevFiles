The statsmodels library provides an implementation of the naive, or classical, decomposition method in a function called [seasonal_decompose()](http://www.statsmodels.org/dev/generated/statsmodels.tsa.seasonal.seasonal_decompose.html). It requires that you specify whether the model is additive or multiplicative.

The _seasonal_decompose()_ function returns a result object. The result object contains arrays to access four pieces of data from the decomposition.
