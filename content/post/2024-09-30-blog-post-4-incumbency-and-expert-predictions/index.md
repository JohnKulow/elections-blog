---
title: 'Blog Post 4: Incumbency and Expert Predictions'
author: John Kulow
date: '2024-09-30'
slug: blog-post-4-incumbency-and-expert-predictions
categories: []
tags: []
---

## Introduction
Being an incumbent President can theoretically have both electoral advantages and electoral disadvantages. On one hand, incumbent presidents start the race with higher name recognition, they can draw the attention of the media easier given their high profile position, they tend to start with a fundraising advantage, they benefit from voters potentially preferring the so-called "devil they know" to the "devil they don't," and they can use so-called "pork barrel" spending to financially benefit crucial voting blogs to try to win over their votes. However, on the other hand, incumbency can prove detrimental in the sense that incumbent presidents can be viewed as responsible for recessions or insufficient responses to natural disasters and they can face potential voter fatigue. Regardless, in recent elections there have been questions of how much incumbency really helps or hurts incumbents given the United States' increasingly polarized electorate. As such, for my fourth blog post I will explore the issue of incumbency, whether it helps or hurts candidates, and how we might think about incumbency in the unique case of the 2024 election.


## Historical Incumbent Advantage
To begin with, let's take a look at the historical trends of incumbency advantage in presidential elections. The table below shows the proportion of incumbent presidents since World War Two who have ran for reelection and won.












```
## Elections with At Least One Incumbent Running: 11
## Incumbent Victories: 7
## Percentage: 63.64
```

As can be seen, of the 11 post-war elections in which the incumbent president ran for reelection, that incumbent won about 64% of the time. The four incumbent presidents who lost were Gerald Ford, Jimmy Carter, George H.W. Bush, and Donald Trump. However, when we look at the win rate of the incumbent *party*, a different narrative emerges.


```
##   reelect_party  N Percent
## 1         FALSE 10   55.56
## 2          TRUE  8   44.44
```

This table shows that, of the 18 post-war presidential elections, the incumbent party has only won 8. As previously shown, 7 of those 8 were times when the incumbent president himself was running, with the 8th case being when George H.W. Bush won following 8 years of being Ronald Reagan's Vice President. This lends credence both to the theory that voters experience voting fatigue for the incumbent party and to the theory that incumbent presidents have a unique strength to them that is different to a successor candidate.

## Pork Barrel Spending Analysis

When trying to see why this might be, many observers often point to so-called "pork barrel spending" which is when politicians use their delineated powers to fund (often frivolous) projects in crucial states or constituencies in order to gain the favor of local voters. To examine whether or not this practice of directing additional funds to swing states actually occurs, I have graphed below federal grant spending between 1988 and 2008, seperated by whether that spending was in a swing state or not and whether the grant occured in an election year or not.


```
## Rows: 1251 Columns: 7
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## chr (3): state_abb, state_year_type, state_year_type2
## dbl (4): year, elxn_year, grant_mil, state_incvote_avglast3
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-7-1.png" width="672" />

As can be seen, there is a statistically significant difference between swing states and non-swing states, with those swing states benefiting from additional grant funding. Interestingly enough, there is not statistically significant difference between grant spending in election years and non-election years. This could be explained by the fact that the projects that these grants fund often take more than a single year to complete, so the community might not see tangible benefits from grant spending within the year, thus yielding little benefit for an incumbent to prioritize grant spending in an election year rather than in the years leading up to it.




```
## Rows: 18465 Columns: 16
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## chr  (3): state, county, state_abb
## dbl (13): year, state_FIPS, county_FIPS, dvoteswing_inc, dpct_grants, dpc_in...
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```

```
## 
## <table style="text-align:center"><caption><strong>County Model Regression Results</strong></caption>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"></td><td><em>Dependent variable:</em></td></tr>
## <tr><td></td><td colspan="1" style="border-bottom: 1px solid black"></td></tr>
## <tr><td style="text-align:left"></td><td>Incumbent Vote Swing</td></tr>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Federal Grants (%)</td><td>0.004<sup>***</sup></td></tr>
## <tr><td style="text-align:left"></td><td>(0.001)</td></tr>
## <tr><td style="text-align:left"></td><td></td></tr>
## <tr><td style="text-align:left">Competitive State</td><td>0.155<sup>*</sup></td></tr>
## <tr><td style="text-align:left"></td><td>(0.077)</td></tr>
## <tr><td style="text-align:left"></td><td></td></tr>
## <tr><td style="text-align:left">Federal Grants * Competitive State</td><td>0.006<sup>***</sup></td></tr>
## <tr><td style="text-align:left"></td><td>(0.002)</td></tr>
## <tr><td style="text-align:left"></td><td></td></tr>
## <tr><td style="text-align:left">Constant</td><td>-6.523<sup>***</sup></td></tr>
## <tr><td style="text-align:left"></td><td>(0.085)</td></tr>
## <tr><td style="text-align:left"></td><td></td></tr>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left">Observations</td><td>17,959</td></tr>
## <tr><td style="text-align:left">R<sup>2</sup></td><td>0.420</td></tr>
## <tr><td style="text-align:left">Adjusted R<sup>2</sup></td><td>0.419</td></tr>
## <tr><td colspan="2" style="border-bottom: 1px solid black"></td></tr><tr><td style="text-align:left"><em>Note:</em></td><td style="text-align:right"><sup>*</sup>p<0.05; <sup>**</sup>p<0.01; <sup>***</sup>p<0.001</td></tr>
## <tr><td style="text-align:left"></td><td style="text-align:right">Standard errors are in parentheses.</td></tr>
## </table>
```





## Incumbency in 2024?






