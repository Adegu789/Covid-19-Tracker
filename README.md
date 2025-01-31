<!-- README.md is generated from README.Rmd. Please edit that file -->

# covid19Tracker

## Installation

#### You need to have R version 4.0.2

Install the development version from [GitHub](https://github.com/) with:

```r
# install.packages("devtools")
devtools::install_github("adegu789/covid19Tracker")
```

## Example

This is a basic example which shows you how to solve a common problem:

```r
library(covid19Tracker)
# Wrong format
period = c("5-6-2020","7-8-2020")
country = "US"
plot <- covid19Tracker::drawCovidPlot(period,country)
#>
#> Attaching package: 'dplyr'
#> The following objects are masked from 'package:stats':
#>
#>     filter, lag
#> The following objects are masked from 'package:base':
#>
#>     intersect, setdiff, setequal, union
#> Warning: package 'GetoptLong' was built under R version 4.0.3
#> -- Attaching packages -------------------- tidyverse 1.3.0 --
#> v ggplot2 3.3.2     v purrr   0.3.4
#> v tibble  3.0.3     v stringr 1.4.0
#> v tidyr   1.1.2     v forcats 0.5.0
#> v readr   1.4.0
#> Warning: package 'ggplot2' was built under R version 4.0.3
#> Warning: package 'readr' was built under R version 4.0.3
#> -- Conflicts ----------------------- tidyverse_conflicts() --
#> x dplyr::filter() masks stats::filter()
#> x dplyr::lag()    masks stats::lag()
#> Warning: package 'reshape' was built under R version 4.0.3
#>
#> Attaching package: 'reshape'
#> The following objects are masked from 'package:tidyr':
#>
#>     expand, smiths
#> The following object is masked from 'package:dplyr':
#>
#>     rename
#> Warning: `summarise_each_()` is deprecated as of dplyr 0.7.0.
#> Please use `across()` instead.
#> This warning is displayed once every 8 hours.
#> Call `lifecycle::last_warnings()` to see where this warning was generated.

####
# You Got error because your date format is not Correct
# Correct format
period = c("05-06-2020","07-08-2020")
country = "US"
plot <- covid19Tracker::drawCovidPlot(period,country)
```

## Lets see an example of world map

```r
map <- covid19Tracker::drawCovidMap("09-09-2020","Deaths")
#>
#> Attaching package: 'RCurl'
#> The following object is masked from 'package:tidyr':
#>
#>     complete
map
```

<img src="man/figures/README-worldMap-1.png" width="100%" />

## You can also embed plots, for example:

<img src="man/figures/README-plot-1.png" width="100%" />
