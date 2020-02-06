---
layout: default
---

<!-- Author: Alfredo Sánchez Alberca (asalber@ceu.es) -->

# R repository

This repository contains a bunch of references, tutorials, courses, recipes, libraries, software tools and other stuff for programming with R.

## References

### Advanced

- [Advanced R](https://adv-r.hadley.nz) Advanced programming topics with R. The solutions to the exercises in this book are in [Advanced R solutions](https://advanced-r-solutions.rbind.io/).
- [R for data science](https://r4ds.had.co.nz/). Advanced applications of R to data science.
- [R packages](http://r-pkgs.had.co.nz/). How to create R packages.

## Courses and tutorials
- [Teacups, Giraffes and Statistics](https://tinystats.github.io/teacups-giraffes-and-statistics/index.html). Original introduction to R and basic Statistics. 

## Packages

- [dplyr](http://dplyr.tidyverse.org/) Data manipulation based on a grammar.
- [ggplot2](http://ggplot2.org/) Plots based on a grammar of graphics.
- [gridExtra](https://cran.r-project.org/web/packages/gridExtra/vignettes/arrangeGrob.html) Arrange different graphics (especially ggplot graphics) and tables in a dashboard.
- [assertr](https://github.com/ropensci/assertr) Data validation.
- [tidylog](https://elbersb.com/public/posts/tidylog100/) Provides feedback for data wrangling operations in R.

## Recipes

- List variables in a data frame.
  ```r
  library(library(tidyverse) 
  data("iris")
  glimpse(iris)
  ```
  ```shell
  Observations: 150
  Variables: 5
  $ Sepal.Length <dbl> 5.1, 4.9, 4.7, 4.6, 5.0, 5.4, 4.6, 5.0, 4.4, 4.9,…
  $ Sepal.Width  <dbl> 3.5, 3.0, 3.2, 3.1, 3.6, 3.9, 3.4, 3.4, 2.9, 3.1,…
  $ Petal.Length <dbl> 1.4, 1.4, 1.3, 1.5, 1.4, 1.7, 1.4, 1.5, 1.4, 1.5,…
  $ Petal.Width  <dbl> 0.2, 0.2, 0.2, 0.2, 0.2, 0.4, 0.3, 0.2, 0.2, 0.1,…
  $ Species      <fct> setosa, setosa, setosa, setosa, setosa, setosa, s…
  ```

- List percentage of missing values in a data frame.
  ```r
  library(tidymodels)
  library(naniar)
  data("credit_data")
  credit_data %>% miss_var_summary()
  ```
  ```shell
  # A tibble: 14 x 3
     variable  n_miss pct_miss
     <chr>      <int>    <dbl>
   1 Income       381   8.55  
   2 Assets        47   1.06  
   3 Debt          18   0.404 
   4 Home           6   0.135 
   5 Job            2   0.0449
   6 Marital        1   0.0225
   7 Status         0   0     
   8 Seniority      0   0     
   9 Time           0   0     
  10 Age            0   0     
  11 Records        0   0     
  12 Expenses       0   0     
  13 Amount         0   0     
  14 Price          0   0   
  ```
  
- Quick data frame summary.
  ```r
  library(tidymodels)
  library(skimr)
  data("credit_data")
  credit_data %>% skim()
  ```
  ```shell
  Skim summary statistics
   n obs: 4454 
   n variables: 14 
  
  ── Variable type:factor   ───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
   variable missing complete    n n_unique                               top_counts ordered
       Home       6     4448 4454        6  own: 2107, ren: 973, par: 783, oth: 319   FALSE
        Job       2     4452 4454        4 fix: 2805, fre: 1024, par: 452, oth: 171   FALSE
    Marital       1     4453 4454        5   mar: 3241, sin: 977, sep: 130, wid: 67   FALSE
    Records       0     4454 4454        2                no: 3681, yes: 773, NA: 0   FALSE
     Status       0     4454 4454        2              goo: 3200, bad: 1254, NA: 0   FALSE
  
  ── Variable type:integer   ──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
    variable missing complete    n    mean       sd  p0     p25  p50    p75  p100     hist
         Age       0     4454 4454   37.08    10.98  18   28      36   45      68 ▅▇▇▇▅▃▂▁
      Amount       0     4454 4454 1038.92   474.55 100  700    1000 1300    5000 ▅▇▃▁▁▁▁▁
      Assets      47     4407 4454 5403.98 11574.42   0    0    3000 6000   3e+05 ▇▁▁▁▁▁▁▁
        Debt      18     4436 4454  343.03  1245.99   0    0       0    0   30000 ▇▁▁▁▁▁▁▁
    Expenses       0     4454 4454   55.57    19.52  35   35      51   72     180 ▇▃▃▁▁▁▁▁
      Income     381     4073 4454  141.69    80.75   6   90     125  170     959 ▇▆▁▁▁▁▁▁
       Price       0     4454 4454 1462.78   628.13 105 1117.25 1400 1691.5 11140 ▇▆▁▁▁▁▁▁
   Seniority       0     4454 4454    7.99     8.17   0    2       5   12      48 ▇▃▂▁▁▁▁▁
        Time       0     4454 4454   46.44    14.66   6   36      48   60      72 ▁▁▂▃▁▃▇▁
  ```

- [Data validation](https://appsilon.com/data-quality/?nabc=1&nabe=4825491004194816:1)


## Software tools

- [Rstudio](https://www.rstudio.com/) IDE for developing with R.

## Other resources

- [Awesome R](https://github.com/qinwf/awesome-R) A github repository with a lot of stuff for R.