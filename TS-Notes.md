Timeseries 101
================

# Summarof Material from Rob Hyndman’s Timeseries Forecasting

More in depth explanations can be located here in his textbook:
<https://otexts.com/fpp2/>

``` r
library(fpp2)
library(dplyr)
```

## Timeseries Analysis Examples

### Basic Plots, outliers, and frequency

``` r
# Plot the three series
autoplot(gold)
```

![](TS-Notes_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

``` r
autoplot(woolyrnq)
```

![](TS-Notes_files/figure-gfm/unnamed-chunk-1-2.png)<!-- -->

``` r
autoplot(gas)
```

![](TS-Notes_files/figure-gfm/unnamed-chunk-1-3.png)<!-- -->

``` r
# Find the outlier in the gold series
goldoutlier <- which.max(gold)
goldoutlier
```

    ## [1] 770

``` r
# Look at the seasonal frequencies of the three series
frequency(gold)
```

    ## [1] 1

``` r
frequency(woolyrnq)
```

    ## [1] 4

``` r
frequency(gas)
```

    ## [1] 12
