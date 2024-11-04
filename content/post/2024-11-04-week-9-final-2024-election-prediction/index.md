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

**National Two-Party Vote Share for the Inc. Party = β~0~ + β~1~Sept. National Polling Average + β~2~Oct. National Polling Average + β~3~Q2 GDP Growth + β~4~Incumbency + ε**



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
- out of sample validation




<img src="{{< blogdown/postref >}}index_files/figure-html/nat model validation graph-1.png" width="672" />




| Harris Vote Share| Lower Bound| Upper Bound|
|-----------------:|-----------:|-----------:|
|          51.82711|    46.55055|    57.10367|

** INSERT PRETTIER GRAPHIC **






<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">State Model Regression Table</caption>
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



<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">State Model (Without Polls) Regression Table</caption>
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





<img src="{{< blogdown/postref >}}index_files/figure-html/combined state pred map-1.png" width="672" />











### Final National Two-Party Vote Prediction



## State-Level Model and Predictions
### Equation and Variables
- Do for both state-level models

### Justrification of Model

### Regression Table
- Include interpretation of coefficients

### Validation
- Out of sample validation

### Final State-Level Two-Party Vote Prediction


## Conclusion







test












