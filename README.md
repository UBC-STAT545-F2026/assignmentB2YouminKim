
<!-- README.md is generated from README.Rmd. Please edit that file -->

# countAllMissingByGroup

<!-- badges: start -->

<!-- badges: end -->

The goal of `countAllMissingByGroup` is to count the number of missing
values for all columns by group

## Installation

You can install the development version of countAllMissingByGroup by
calling:

``` r
devtools::install_github("UBC-STAT545-F2026/assignmentB2YouminKim",ref="0.1.0")
```

## Example

This is a basic example which computes the number of missing values in
the `airquality` dataset grouped by the `Month` column.

``` r
library(countAllMissingByGroup)

# Find the number of missing observations within each month in the airquality part of datasets
count_all_missing_by_group(airquality, Month)
#> # A tibble: 5 × 6
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0

# An alternative way of invoking the `count_all_missing_by_group()`: piping the dataset into the function. 
airquality |> count_all_missing_by_group(Month) 
#> # A tibble: 5 × 6
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0
```
