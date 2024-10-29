---
title: 'Blog Post 8: Shocks'
author: John Kulow
date: '2024-10-28'
slug: blog-post-8-shocks-and-penultimate-model
categories: []
tags: []
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />



## Introduction

We are now only one week away from the election. Thus, this week I will first briefly explore the role that so-called "shocks" and "October Surprises" have on elections. Every election year, unexpected  events happen that may or may not significantly affect the election, but they are usually near impossible to predict and/or equally hard to quantify, which is why I will discuss their role generally in elections and discuss some events in the 2024 campaign that could be considered "shocks" before then dedicating more time to updating my model and expanding it to all 50 states. 


## Shocks

Historically, people have argued that things as seemingly small and apolitical as high school football game victories and shark attacks and that things as monumental and/or calamitous as hurricanes and pandemics should be considered "shocks." As we have discussed in class, the actual effects of smaller, more localized events, like the first two examples, is heavily disputed. However, many larger apolitical events like natural disasters and, predictably, many notable political events (particularly those that occur in the final month of the campaign) clearly have impacts.

Obviously, it is almost impossible to determine any causal effects from these shocks and October surprises, but let's briefly explore some key events from the 2024 election that we may consider to be shocks. In terms of political events, we can definitively say that Biden's performance in the first presidential debate and his subsequent withdrawal from the race were sudden shocks that upended the race. There were also some political shocks whose effects are unclear, such as the two assassination attempts against Trump. There also have, and in the next week likely will be more, political shocks happening in the home stretch, such as the anti-Puerto Rican joke made at Trump's Madison Square Garden rally the night of the 27th, and we will not know the effects of the these late-emerging shocks until after the election, if ever. In terms of apolitical shocks from this cycle, the clear frontrunner is Hurricane Helene, which wroght destruction to much of western North Carolina and parts of Georgia, two crucial swing states in the election. Already, there are reports of lower turnout in the affected regions, which, in a close election, might prove decisive.





## Electoral Model
### National 2-Party Popular Vote Model

For my national model, I have updated it to include new polling additions from the last week. I played around with adding certain other variable, such as the incumbent president's approval rating and quarter 2 RDI growth, but I decided against including these because, in the case of the former, I believe President Biden's approval numbers are disproportionately dragged down by perceived ineffectiveness of his age and that Harris, who enjoys on average an even (if not positive) approval rating is uniquely insulated from this outlier data point compared to prior elections. In the case of the latter, I chose not to include RDI growth given previously concerns about how predictive it is and whether it overlaps too much with GDP growth. I also made the decision, unlike my model from last week, to exclude the 2020 election from my model. This is because I believe that the economic outlier situation in 2020 was unrepresentitve of typical trends. As such, below is the regression table for my updated model:





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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.21</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.28</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.87&nbsp;&ndash;&nbsp;0.45</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.484</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.61</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.26</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.01&nbsp;&ndash;&nbsp;1.22</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.048</strong></td>
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

As can be seen, my model is still a significant predictor of past election results, with an adjusted R squared value of 0.917. When applied to 2024 polling data, GDP growth, and incumbency, I predict the following share of the two party national popular vote for Harris:




| Harris Vote Share| Lower Bound| Upper Bound|
|-----------------:|-----------:|-----------:|
|           51.8823|    46.60423|    57.16036|

This represents about a 1 point decrease in her share of the 2-party national popular vote compared to my model last week, though the upper and lower bounds clearly show that it is clearly possible for Harris to win by more come next Tuesday night or to outright lose the national popular vote.

### State 2-Party Model and Electoral College

Moving on to my state-level model, I have made a few changes this week. First, I have added in electoral lag into my model, adding in variables that factor in how states voted in 2020 and 2016. In addition to that, I have continued to include the September and October polling numbers, the GDP quarter 2 growth, and the incumbency factor into my model below:




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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;3.47</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.00</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;5.44&nbsp;&ndash;&nbsp;-1.49</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.15</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.11</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.36&nbsp;&ndash;&nbsp;0.07</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.178</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.95</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.12</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.72&nbsp;&ndash;&nbsp;1.18</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag1</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.32</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.06</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.21&nbsp;&ndash;&nbsp;0.44</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag2</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.02</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.04</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.06&nbsp;&ndash;&nbsp;0.10</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.563</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">GDP growth quarterly</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.10</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.02</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.07&nbsp;&ndash;&nbsp;0.13</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">d incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.88</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.47</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;1.81&nbsp;&ndash;&nbsp;0.04</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.061</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">290</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.935 / 0.934</td>
</tr>

</table>

As can be seen above, my model is one again highly predictive, with an adjusted R squared value of 0.934. When applying this to the 2024 election for states that we have polling for, we get the following:



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
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.99701 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 45.96480 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.02922 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> California </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 66.35129 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 61.25790 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 71.44468 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Florida </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 49.42892 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 44.38904 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 54.46879 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Georgia </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.30020 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 46.26385 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.33655 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Maryland </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 69.09056 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 64.00166 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 74.17946 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Michigan </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 52.37408 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 47.33991 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.40825 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Minnesota </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.68925 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 49.65307 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.72543 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Missouri </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 44.02709 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 38.97850 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 49.07567 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Montana </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.79470 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 36.76266 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.82674 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Nebraska </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 40.72778 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 35.68590 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 45.76965 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Nebraska Cd 2 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.44722 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.39503 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.49942 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Nevada </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 52.32526 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 47.28961 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.36092 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New Hampshire </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.66123 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.61341 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.70904 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New Mexico </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.59479 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.56292 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.62667 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New York </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.74034 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.68942 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 65.79125 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> North Carolina </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.20562 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 46.16098 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.25026 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Ohio </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.74829 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.71675 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 51.77983 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Pennsylvania </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 52.17702 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 47.13659 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.21746 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Texas </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 47.92379 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 42.89250 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 52.95508 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Virginia </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 55.46919 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.44100 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.49738 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Wisconsin </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 52.23845 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 47.18666 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.29024 </td>
  </tr>
</tbody>
</table>

As can be seen, not only do we have a few more states represented here than my model from last week, but we also have some shifts. Notably, Florida has now shifted out of Harris' column into Trump's, with Texas and Ohio falling deeper into his column and the 7 key swing states all falling back within a 5-point margin, with Arizona now under a 2-point margin.

Another key change I have made to my model this week is that I have added in a secondary model for states that do not have polling available for the 2024 election. This model thus includes the other four variables I put into my first state-level model. The regression table for this second model is below:



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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">3.57</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.04</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.51&nbsp;&ndash;&nbsp;5.62</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag1</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.11</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.00&nbsp;&ndash;&nbsp;1.21</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag2</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.13</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.24&nbsp;&ndash;&nbsp;-0.02</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.016</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">GDP growth quarterly</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.01</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.02</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.02&nbsp;&ndash;&nbsp;0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.490</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">d incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;4.63</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.53</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;5.67&nbsp;&ndash;&nbsp;-3.58</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">255</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.918 / 0.917</td>
</tr>

</table>

As can be seen, this model is still highly predictive of results, albeit slightly less than the first model and relying heavily on the 1-cycle lag variable. Nonetheless, it is a useful indicator, and when I apply this to 2024 numbers for the states without polling numbers and map the results of the results of the two models, we get the below electoral map:







<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-16-1.png" width="672" />

This map (which does not show Trump-won Alaska or Harris-won Hawaii or DC, and which does also not show margins in NE02 or ME02, which would go to Harris and Trump respectively) shows a Harris electoral college victory 319-219 over Trump.



























