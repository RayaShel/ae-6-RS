Nobel winners
================
Raya Shelashska

``` r
library(tidyverse)
```

Let’s first load the data:

``` r
nobel <- read_csv("data-raw/nobel.csv")
```

    ## Rows: 935 Columns: 26
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr  (21): firstname, surname, category, affiliation, city, country, gender,...
    ## dbl   (3): id, year, share
    ## date  (2): born_date, died_date
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

Then let’s split the data into two:

``` r
nobel_stem <- nobel %>%
  filter(category %in% c("Physics", "Chemistry", "Medicine", "Economics"))

nobel_nonstem <- nobel %>%
  filter(!(category %in% c("Physics", "Chemistry", "Medicine", "Economics")))
```

And finally write out the data:

``` r
# add code for writing out the two data frames here
```
