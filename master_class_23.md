# 23 Time Series Analysis
## Daniel Burrueco

* We'll work with dataframes/series with the timestamp in the index

* python package ```statsmodel``` is able to use classes for SARIMAX and all the other underlying algorithms (AR, MA, ARMA, etc.) We'll only use ```statsmodel``` for this reason

* ```pd.timestamp``` means an exact moment, up to nanoseconds. ```date```in ```datetime``` library is just a day

* We can convert ```date```into ```pd.timestamp``` with ```pd.Timestamp(date(2019, 8, 26))```

* ```date_range``` and ```period_range``` are useful for generate date indices. 4 values: start, end, periods, freq. Can only use 3 setting values at a time





