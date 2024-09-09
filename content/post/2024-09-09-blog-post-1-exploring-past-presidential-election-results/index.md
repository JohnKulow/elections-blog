---
title: 'Blog Post 1: Exploring Past Presidential Election Results'
author: John Kulow
date: 'September 9th, 2024'
slug: blog-post-1-exploring-past-presidential-election-results
categories: []
tags: []
---

## **Introduction**

In this first blog post, I seek to gain a better understanding of past U.S. presidential elections that have taken place after World War Two. This analysis, which will include an exploration of national popular vote margins, state-level margins, and state-level swings, will help guide my first predictive model for the 2024 presidential election.

## **Historical Two-Party Vote Share**
### National Results:

insert national 2pv paragraph here




``` r
library(ggplot2)
library(maps)
library(tidyverse)
```

```
## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
## ✔ dplyr     1.1.4     ✔ readr     2.1.5
## ✔ forcats   1.0.0     ✔ stringr   1.5.1
## ✔ lubridate 1.9.3     ✔ tibble    3.2.1
## ✔ purrr     1.0.2     ✔ tidyr     1.3.1
## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
## ✖ dplyr::filter() masks stats::filter()
## ✖ dplyr::lag()    masks stats::lag()
## ✖ purrr::map()    masks maps::map()
## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
```


``` r
d_popvote <- read_csv("data/popvote_1948-2020.csv")
```

```
## Rows: 38 Columns: 9
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## chr (2): party, candidate
## dbl (3): year, pv, pv2p
## lgl (4): winner, incumbent, incumbent_party, prev_admin
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```

``` r
d_popvote_wide <- d_popvote |>
    select(year, party, pv2p) |>
    pivot_wider(names_from = party, values_from = pv2p)
d_popvote_wide <- d_popvote_wide |> 
    mutate(winner = case_when(democrat > republican ~ "D",
                              TRUE ~ "R"))
```


``` r
d_popvote |>
  ggplot(aes(x = year, y = pv2p, color = party)) +
  geom_line() + 
  scale_color_manual(values = c("dodgerblue4", "firebrick1")) +
  theme_bw()
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" width="672" />


### State-Level Results:

insert state winner and state margin paragraphs here

### State-Level Swings:

insert state swing paragraph here

## **Initial Predictions**
### Prediction 1: Based off of Past Election Results

Prediction one paragraph here

### Prediction 2: Adding in OLS

OLS prediction 2 paragraph here









