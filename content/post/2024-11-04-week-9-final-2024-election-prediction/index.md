---
title: 'Blog Post 9: Final 2024 Election Prediction'
author: John Kulow
date: '2024-11-04'
slug: week-9-final-2024-election-prediction
categories: []
tags: []
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />

## Introduction
For this week's blog post, the day before the 2024 election, I will make my final predictions for the national two-party popular vote, state-level two-party popular vote shares, and the associated electoral college vote. Altogether, my predictions are based off of three models, all multivariate ordinary least squares (OLS) regression models, that hopefully together will paint an accurate picture of what the results will be tomorrow (or whenever we actually end up getting results).


## National Model and Prediction
### Equation and Variables
Let's begin with my national popular vote prediction. This model is built to predict what percentage of the two-party national popular vote will go to the candidate from the incumbent party. This vote share is the dependent variable. In terms of independent variables for this OLS model, I used the following four:

- ***October Polling Average***: The average of national polls taken in October, as compiled by 538, and weighted by how many weeks were left until the election.
- ***September Polling Average***: The average of national polls taken in *September*, as compiled by 538, and weighted by how many weeks were left until the election.
- ***Quarter 2 GDP Growth***: The percent national GDP growth in Q2 of the respective election year, as provided by the Federal Reserve.
- ***Incumbency***: If the candidate is the incumbent president or not (in addition to being from the incumbent party).

Thus together, the equation for my model is:

**National Two-Party Vote Share for the Inc. Party = β**~0~ **+ β**~1~**Oct. National Polling Average + β**~2~**Sept. National Polling Average + β**~3~**Q2 GDP Growth + β**~4~**Incumbency + ε**


### Justification of National Model
**October Polling Average**:
Although the accuracy of political polling has been repeatedly called into question, especially over the past few years following notable mishaps in the polling industry in 2016 and 2020, they remain perhaps our best indicator of what electorates are believing at any given point. This said, polling tends to become more accurate as election day approaches, as found by [Gelman and King
(1993)](https://gking.harvard.edu/files/bj215.pdf). This is why I have weighted my October polling average by each day, favoring polls on days closer to election day.

**September Polling Average**:
I made the decision to include a *September* polling average, despite Gelman and King's findings, because of recent criticisms within the polling industry about two things. First, there are concerns about poll "herding" as the election gets near, with polling agencies being accused of ignoring results that would be outliers and favoring results that either align with other polls or show a closer race. Particularly after the polls supposedly missed in 2016 and 2020, some believe that polling firms are showing a tightening race between Harris and Trump in the last month because these polling agencies got burnt in the last two presidential cycles by overestimating Democrats' strength and would rather underestimate Harris than once again overestimate Democrats. The second reason is that in recent cycles, *particularly* in 2022, we have influxes of partisan-funded polls right before the election with the accused intention of wanting to artificially change poll averages to favor their candidate. Thus, for both of these reasons, I wanted to include a September polling average independent variable, knowing that historically it was a worse predictor, because I am concerned for the above two reasons that October polling may be less accurate this time around. By including an average from September, from before polling began to herd and be biased by partisan polls supposedly, I hope to mitigate the impact on my model that any incorrect last-minute shift in the polls may bring.

**Quarter 2 GDP Growth**:
As always, the economy is front and center in politics in 2024. Voters care about the strength in the economy, and, as [Achen and Bartels
(2014)](https://press.princeton.edu/books/hardcover/9780691169446/democracy-for-realists?srsltid=AfmBOorl6iN4qgweThT5hVNygA3GYiEx8IZYUksJEgexdWLE3Es2imza) note, if the economy is weak then voters tend to blame the incumbent party. If the economy is strong, on the other hand, the incumbent party does relatively better. As explored in previous blog posts, I have settled on using Quarter 2 GDP Growth as a barometer for the economic fundamentals of a campaign both because it has a better predictive track record based off of past elections but also because I believe it is a better, more holistic measurement of strength in the economy rather than other proposed measures such as RDI growth. Quarter 2 is used here because it is recent enough to be in voter's memories, but long enough ago that it defines their perception of the economy under the incumbent party in a way that Q3 would not, as any sudden upswing or downturn in Q3 could likely be waved off by the incumbent party as having been out of their control, or the effects of such a change in the economy may not have had time to trickle down to voters just yet.

**Incumbency**:
Although literature and expert opinions on the role of incumbency are split on whether it has an affect and, if so, whether such an effect is positive or negative. Some claim that the President's superior ability to fund-raise, to gain free media attention, and to otherwise wield the powers of the Presidency to the advantage of them or of their constituents/potential supporters gives the incumbent president an advantage going into reelection. Others claim that voters can blame the president for any problems facing the country. Others believe any such impact one way or the other is minute, irrelevant, or self-balanced. I believe that the role of incumbency does matter, which is why I have included it in my model, and that we need to look no further than President Biden's dramatic exit from the 2024 race this past summer to see the importance of whether an incumbent president, for all their faults or strengths, runs for reelection.


### Regression Table
I based my model off of data spanning from 1968, when polling data from 538 begins, to the 2016 election. I made the decision to exclude the 2020 election because the economic data from Quarter 2 is such an outlier due to the Covid pandemic that it substantively, and in my opinion unrepresentatively, changed my model when included. Thus, based off of the aforementioned four independent variables and the 13 elections spanning 1968-2016, below is the regression table for my model:









<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">National Model Regression Table</caption>
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="4" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">National 2-Party Vote Share for Incumbent Party</th>
</tr>
<tr>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  text-align:left; ">Predictors</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">Estimates</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">std. Error</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">CI</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">p</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">(Intercept)</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">30.87</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">3.75</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">22.22&nbsp;&ndash;&nbsp;39.52</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.61</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.26</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.01&nbsp;&ndash;&nbsp;1.22</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.048</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.21</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.28</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.87&nbsp;&ndash;&nbsp;0.45</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.484</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">GDP growth quarterly</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.45</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.17</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.07&nbsp;&ndash;&nbsp;0.83</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.025</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.00</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.27</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;1.94&nbsp;&ndash;&nbsp;3.93</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.456</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">13</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.891 / 0.836</td>
</tr>

</table>

In terms of how we interpret the above coefficients for each of the four IV's:
**October Polling Average**: For every 1-point increase in the incumbent candidate's weighted October national polling average, we can expect an 0.61-point increase in their eventual national two-party vote share. With a p-value of 0.048, this is one of the two statistically significant IV's in my model at a 95% confidence interval.

**September Polling Average**: For every 1-point increase in the incumbent candidate's weighted September national polling average, we can expect an 0.21-point decrease in their eventual national two-party vote share *when controlling for other variables including the October polling average*. This last point is important to note. With a p-value of 0.484, this is not statistically significant , but that does not mean that the inclusion of this variable does not add value to my model, as explained previously.

**Quarter 2 GDP Growth**: For every 1% increase in Quarter 2 GDP growth, there is an associated 0.45-point increase in the incumbent party candidate's November national two-party vote share. With a p-value of 0.025, this is the second of the two statistically significant IV's in my model at a 95% confidence interval.

**Incumbency**: For every 1% increase in "incumbency" there is an associated 1.00-point increase in the incumbent party candidate's national two-party vote share. This may not initially make much sense, but consider that, of course, there is no such thing as a "1% increase in incumbency" as this is a binary variable. With a p-value of 0.456, this too is not statistically significant at a 95% confidence interval, but just like the September polling average, that does not mean it does not add value to my model.


### Validation
For in-sample error, my model's R-squared value of 0.89 means that 89% of changes in national two-party popular vote share is explained by my model, representing a pretty strong correlation. This correlation holds strong when adjusted, with an adjusted R-squared value of 0.84.

To understand my out-of-sample error, I performed 1,000 repetitions of random sampling, with each sample using 7 elections, which is slightly over half of the 13 total in the time frame of my data set. The average mean out-of-sample error, as shown by the black line in the graph below, is ~3.81%, a reasonably low number. 



<img src="{{< blogdown/postref >}}index_files/figure-html/nat model validation graph-1.png" width="672" />

The above histogram shows the distribution of these mean errors. I have limited the x-axis of this graph to a reasonable range, so there are one or two outlier data points not shown above, though they are incorporated into the calculation of the average mean absolute error. I have restricted the x-axis so that we can better see that this graph is right-skewed. While there certainly are some outlier data points where my model failed to accurately predict the election, those are far outnumbered by instances of my model accurately capturing the state of the race.


### Final National Two-Party Vote Prediction

Given this model, when we apply this result to the 2024 election between Vice President Harris and Former President Trump, we get the following prediction:




| Harris Vote Share | Lower Bound | Upper Bound |
|:-----------------:|:-----------:|:-----------:|
|     51.82711      |  46.55055   |  57.10367   |

As can be seen, my model predicts that Vice President Harris will win the national popular vote with **51.83%** of the vote, a **3.66% margin** over Former President Trump and his **48.17%** share. There is still a relatively large range of possibilities considering today's polarized political climate, with the upper bound of Harris' vote share with a 95% confidence interval being 57.1% and the lower bound being 46.55%, meaning Harris could win by up to a 14.2% margin or lose by up to a 6.9% margin. Thus, to get an even better sense of the state of the race, it is important to now turn to the state level.



## State-Level Model and Predictions
### Equation and Variables

For my state-level analysis, I used two models, with both being OLS regression models built to predict what percentage of the state-level two-party popular vote the Democratic nominee should receive. The first is the primary model, and it uses the following six independent variables:

- **October State-Level Polling Average**: The average of state-level polls taken in October, as compiled by 538, and weighted by how many weeks were left until the election.
- **September State-Level Polling Average**: The average of national polls taken in *September*, as compiled by 538, and weighted by how many weeks were left until the election. For the roughly 3 states (none of which considered swing states) and 1 district (Maine's 2nd) for which there were not any polls released in September but did have October polls, I set their September Polling Average to equal their October average so as to allow them to be included in the model.
- **One Cycle Democratic Vote Lag**: The Democratic candidate's share of the two-party popular vote in the state in the presidential election immediately prior.
- **Two Cycle Democratic Vote Lag**: The Democratic candidate's share of the two-party popular vote in the state in the presidential election two cycles (eight years) ago.
- **Incumbent Party Status**: Whether or not Democrats held the Presidency in the term leading up to the election.
- **National October Polling Average**: The average of *national* polls taken in October, as compiled by 538, and weighted by how many weeks were left until the election.

Taken together, the equation for my primary state-level model is:

**State Two-Party Vote Share for the Democratic Nominee = β**~0~ **+ β**~1~**Oct. State-Level Polling Avg. + β**~2~**Sept. State-Level Polling Avg. + β**~3~**One-Cycle Dem. Vote Lag + β**~4~**Two-Cycle Dem. Vote Lag + β**~5~**Inc. Party Status + β**~6~**Oct. National Polling Avg. + ε**


### Justification of Model

**State-Level Polling**: As you can see, there are a number of similarities between my national and state models. As previously explained, despite its flaws polling is still a strong indicator of results, and state-level polling is  a good indicator historically of how that state will vote. For the same reasons as my national model, I included variables for both October and September averages. 

**Democratic Vote Lag**: I added two new variables representing past election results in that state. While states certainly swing from year to year, most voters do not change their minds, so the last election, especially in today's polarized political climate, tends to be a good indicator of future results. I included the *two cycle* lag variable for a slightly different reason. Including this variable bakes into my model how much the state shifted left or right going into the last election. While many states may only move slightly or may bounce around depending on the year, some other states (ie. Alaska, Texas, Massachusetts) have fairly consistently trended left in recent cycles, while others (ie. Arkansas, Nevada, Florida) have trended rightwards relative to the nation. These trends tend to be because of gradual demographic changes within these states (such as Texas' rapid growth and diversification) or because of gradual realignments in the composition of the two parties' political bases (such as Democrats' gradual growth among high-education suburbanites). As such, I felt it important to add a second variable to include a measurement of these trends.

**Incumbency**: Here I have factored in incumbency slightly differently than in my national model. Since my national model was based around the incumbent party, it was important to test whether the candidate themselves were an incumbent running for reelection or not. Now that my model is based around *Democratic* vote share, I felt it was more important to focus on party incumbency more generally.

**National Polling**: Obviously this is a state-level model, but I wanted to factor in a variable for national polling averages, since in 2024 we find ourselves in an election where the national polling environment indicates a shift rightwards from 2020, but state-level polling largely has remained stable compared to last cycle's results. Thus, I feel like it is important to test the effects of both since, although they overlap slightly, in tandem they may catch trends previously left unnoticed.


Unfortunately however, this model only can be applied to the relatively few states for which we have publicly available polling. There are many states that are considered to be safely in Democrats' or Republicans' aisles that no polling firms has decided to invest resources in polling for non-internal purposes. Thus, knowing that these safe states will not affect my electoral college prediction I decided to make a ***second***, slightly simpler model for them. This supplementary OLS model drops the variables for October and September state-level polling averages, but it adds back in the national September polling average IV from my national model so as to replicate the potential September effects I explained above. In my primary state-level model, I decided that the inclusion of only the state-level September polling was sufficient and thus did not include the national September polling average in that primary model.



<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">(Primary) State Model Regression Table</caption>
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="4" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">State 2-Party Vote Share for Democrats</th>
</tr>
<tr>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  text-align:left; ">Predictors</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">Estimates</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">std. Error</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">CI</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">p</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">(Intercept)</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">7.51</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">5.07</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;2.47&nbsp;&ndash;&nbsp;17.50</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.140</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.18</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.11</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.40&nbsp;&ndash;&nbsp;0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.118</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.95</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.13</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.70&nbsp;&ndash;&nbsp;1.19</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag1</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.38</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.06</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.26&nbsp;&ndash;&nbsp;0.50</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag2</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.01</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.10&nbsp;&ndash;&nbsp;0.08</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.835</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">d incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.95</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.52</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;1.98&nbsp;&ndash;&nbsp;0.08</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.070</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">nat oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.22</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.10</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.43&nbsp;&ndash;&nbsp;-0.02</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.033</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">290</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.928 / 0.926</td>
</tr>

</table>



<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">(Supplementary) State Model Regression Table</caption>
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="4" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">State 2-Party Vote Share for Democrats</th>
</tr>
<tr>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  text-align:left; ">Predictors</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">Estimates</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">std. Error</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">CI</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">p</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">(Intercept)</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;30.82</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">5.88</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;42.41&nbsp;&ndash;&nbsp;-19.24</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag1</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.09</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.99&nbsp;&ndash;&nbsp;1.20</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag2</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.11</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.06</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.22&nbsp;&ndash;&nbsp;0.01</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.062</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">d incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;1.83</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.59</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;3.00&nbsp;&ndash;&nbsp;-0.66</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.002</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">nat sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;1.63</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.23</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;2.08&nbsp;&ndash;&nbsp;-1.18</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">nat oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">2.26</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.28</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.71&nbsp;&ndash;&nbsp;2.82</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">255</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.935 / 0.934</td>
</tr>

</table>










<img src="{{< blogdown/postref >}}index_files/figure-html/state validation graph-1.png" width="672" />



<table>
 <thead>
  <tr>
   <th style="text-align:left;"> State </th>
   <th style="text-align:right;"> Harris Vote Share </th>
   <th style="text-align:right;"> Lower Bound </th>
   <th style="text-align:right;"> Upper Bound </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Arizona </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.17068 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 44.85019 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.49117 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> California </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 65.17024 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.78080 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 70.55968 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Florida </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 48.36540 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 43.03339 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 53.69742 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Georgia </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.42399 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 45.10149 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.74650 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Indiana </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.34649 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 36.02409 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.66890 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Maine Cd 2 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.58067 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.26204 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 51.89930 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Maryland </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 68.04048 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 62.66586 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 73.41510 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Massachusetts </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 66.76200 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 61.39923 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 72.12476 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Michigan </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.44157 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 46.11853 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.76461 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Minnesota </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 53.89702 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 48.57408 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.21996 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Missouri </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 43.16617 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 37.83319 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 48.49915 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Montana </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.09607 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 35.77414 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.41800 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Nebraska </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 40.09414 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 34.76453 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 45.42374 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Nebraska Cd 2 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.57686 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 49.24191 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.91181 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Nevada </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.36874 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 46.04218 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.69530 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New Hampshire </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.67997 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 49.34864 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.01130 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New Mexico </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.62405 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 49.29581 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.95228 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New York </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.86333 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.49855 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 65.22812 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> North Carolina </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.31757 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 44.98784 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.64730 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Ohio </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.02362 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 40.70049 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 51.34675 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Pennsylvania </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.23316 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 45.90608 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.56025 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Texas </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 47.12235 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.80247 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 52.44224 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Virginia </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.64381 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 49.32428 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.96335 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Washington </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.57076 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.22182 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 65.91970 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Wisconsin </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.20178 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 45.86424 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.53932 </td>
  </tr>
</tbody>
</table>





<img src="{{< blogdown/postref >}}index_files/figure-html/combined state pred map-1.png" width="672" />






- Do for both state-level models



### Regression Table
- Include interpretation of coefficients

### Validation
- Out of sample validation

### Final State-Level Two-Party Vote Prediction


## Conclusion







test












