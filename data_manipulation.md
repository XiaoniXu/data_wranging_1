Data Manipulation
================

9/17/2024 The days are getting shorter 9/19/2024 The sun will die

This document will show how to **manipulate** data.

``` r
litters_df = 
  read_csv("data/FAS_litters.csv", na = c("NA", "", "."))
```

    ## Rows: 49 Columns: 8
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (2): Group, Litter Number
    ## dbl (6): GD0 weight, GD18 weight, GD of Birth, Pups born alive, Pups dead @ ...
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
litters_df = janitor::clean_names(litters_df)

pups_df = 
  read_csv("data/FAS_pups.csv", na = c("NA", "", "."))
```

    ## Rows: 313 Columns: 6
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (1): Litter Number
    ## dbl (5): Sex, PD ears, PD eyes, PD pivot, PD walk
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
pups_df = janitor::clean_names(pups_df)
```

## ‘select’

Use ‘select()’ to select variables

``` r
select(litters_df)
```

    ## # A tibble: 49 × 0

## ‘filter’

## ‘mutate’

## ‘arrange’
