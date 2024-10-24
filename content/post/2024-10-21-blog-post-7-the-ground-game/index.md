---
title: 'Blog Post 7: The Ground Game'
author: John Kulow
date: '2024-10-21'
slug: blog-post-7-the-ground-game
categories: []
tags: []
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />




## Introduction

Campaigns every year spend billions of dollars trying to convince registered voters to both turn out and choose their prefered candidate. While the largest campaign expense every year is the air war, which I covered last week, campaigns also spend significant resources trying to win the so-called "Ground Game." This week, I will look into the role of field offices and campaign stops before then updating my national popular vote model and state by state model.

## The Ground Game
### Field Offices

To begin our analysis of the ground game, let's explore the role that field offices play. These offices serve as the local hubs for campaigns and their volunteers to go out and knock on doors, put up signs, and generally conduct what many people see as the on the ground element of a campaign. Obviously, not having a physical presence in an area means that you are not fighting on the ground for those voters' support, whereas if both campaigns have numerous offices in an area it is clear how contested that region is. Let's look at the geographic distribution of field offices in 2012 and 2016.







<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-4-1.png" width="672" />

Above we can see the shifting nature of where the campaigns considered to be battleground states. In 2012, Obama had numerous field offices in Dem-leaning states like New Mexico, Colorado, and Oregon while in 2016 Clinton pulled back her efforts in those states. We also can see the emergence of Arizona as a battleground, with Romney not having any Arizona field offices in 2012 but Trump ramping up efforts in the state four years later, with the inverse being true for Maine, where Obama barely had any offices and Romney did not contend, but Clinton had to defend the state heavily and only won by a 3% margin.








We can also look closer within states. For example, in the perennial battleground state of Wisconsin, the 2016 Clinton campaign had notably fewer field offices, particularly in numerous rural areas in the north, northwest, and southwest. This change, as can be seen in the graphs below, correlated with a massive Democratic collapse in rural areas. Of course, this is not entirely due to the reduced ground presence, as Democratic collapse among working-class white voters in 2016 happened across the board. Even if one were to claim that there is no causal effect, it is clear that field offices are important for understanding campaigns' strategies.



<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-9-1.png" width="672" />


### Campaign Events

Another crucial way that the group war is waged is with campaign events involving the candidate themselves. We can first graph these events over time. In the three graphs below, we can see how the number of these campaign events ramp up in the final month or so, and now during the 2024 cycle we can see the beginnings of this upswing in events too.




```
## `geom_smooth()` using method = 'loess' and formula = 'y ~ x'
## `geom_smooth()` using method = 'loess' and formula = 'y ~ x'
## `geom_smooth()` using method = 'loess' and formula = 'y ~ x'
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-11-1.png" width="672" />

Obviously though, campaign events are tied to specific locations, meaning we can plot where on the map these events take place, which I have done below for the 2016, 2020, and 2024 (so far). Once again, and even moreso than with the field offices map, we can see how these campaigns strategically target events in the states they view as competitive, with the Midwest battlegrounds, North Carolina, Nevada, Arizona, and (to a lesser extent in 2016) Georgia featuring heavily in all three election cycles. We also can clearly see how neither campaign believes that Florida is in play this cycle, or at least not in play enough to warrent spending the principle's valuable time.



<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-13-1.png" width="672" />

## Updating Models
### National 2-Party Popular Vote Model

Finally, it is time for me to update my 2024 model. This week I am combining updated polling data but also factoring in Quarter 2 economic performance and the incumbency effect. Now that we are only about 2 weeks away from the election, we are beginning to incorporate polls that are being weighed heavily due to the historical accuracy of polls near to election day.



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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">28.28</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">4.20</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">18.78&nbsp;&ndash;&nbsp;37.79</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.01</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.32</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.73&nbsp;&ndash;&nbsp;0.71</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.977</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.51</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.31</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.18&nbsp;&ndash;&nbsp;1.20</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.130</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">GDP growth quarterly</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.13</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.08</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.05&nbsp;&ndash;&nbsp;0.30</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.132</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.35</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.46</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;2.96&nbsp;&ndash;&nbsp;3.65</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.818</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">14</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.835 / 0.762</td>
</tr>

</table>

This model has an R squared value of 0.84 and an adjusted R squared value of 0.76, meaning that there is likely a strong predictive effect of the model. This said, these R squared values are lower than they might otherwise be because of the presence of the 2020 GDP growth outlier data point, but I made the decision to include that data point because even if it might make my trendline fit slightly less well, the chaotic nature of today's politics and economic realities may mean that the predictive power of Q2 GDP growth moving forward may be more in line with the 2020 effects than with prior trends, and I wanted to incorporate that uncertainty into my model.

If we then use 2024 data, including 2024 polling data up until this day, we get the following national 2-party vote share result for Harris:




| Harris Vote Share| Lower Bound| Upper Bound|
|-----------------:|-----------:|-----------:|
|          52.85314|    46.85147|    58.85482|

This would represent about a 5.5% 2-party national vote share victory over Trump, which although a slight decrease from Biden's 2020 margin, still represents a strong national popular vote victory in today's calcified political environment. This model also has more constrained bounds than many of my previous models, which is of note.

### State 2-Party Model and Electoral College

Moving on to the state level, I use the same variables: polling data, GDP performance, and incumbency effect.



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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;2.76</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.25</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;5.22&nbsp;&ndash;&nbsp;-0.31</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>0.028</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">sept poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.17</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.29&nbsp;&ndash;&nbsp;0.38</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.779</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">oct poll</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.13</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.16</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.81&nbsp;&ndash;&nbsp;1.45</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">GDP growth quarterly</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.17</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.02</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.13&nbsp;&ndash;&nbsp;0.21</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">d incumbent</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.18</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.52</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.85&nbsp;&ndash;&nbsp;1.21</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.727</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">191</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.921 / 0.919</td>
</tr>

</table>

This model seems even more predictive, with an R squared value and an adjusted R squared value of 0.92, with state level October polling being particularly predictive. When we apply 2024 data to this model we get the following results: 



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
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 52.79599 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 46.92425 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 58.66774 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> California </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 67.66514 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 61.72463 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 73.60564 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Florida </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.26466 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 45.40155 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.12777 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Georgia </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 53.29166 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 47.41821 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.16511 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Maryland </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 70.70724 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 64.74939 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 76.66510 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Michigan </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.13417 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 48.26183 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.00652 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Minnesota </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.42838 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.55066 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 62.30610 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Missouri </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 46.66412 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 40.79641 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 52.53183 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Montana </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 43.65292 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 37.78582 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 49.52002 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Nebraska </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 41.07555 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 27.31091 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 54.84020 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Nebraska Cd 2 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.78784 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.90186 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 63.67381 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Nevada </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 53.95362 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 48.09405 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.81318 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New Hampshire </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 57.83063 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 51.94734 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 63.71392 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New Mexico </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.74991 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.86887 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 62.63095 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> New York </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 58.47675 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 40.20306 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 76.75044 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> North Carolina </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 53.45914 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 47.59041 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 59.32787 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Ohio </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 48.54860 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 42.68988 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 54.40733 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Pennsylvania </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.18112 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 48.31485 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.04740 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 221, 221, 255) !important;"> Texas </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 49.81926 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 43.95067 </td>
   <td style="text-align:right;background-color: rgba(255, 221, 221, 255) !important;"> 55.68786 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Virginia </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 56.72388 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 50.85122 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 62.59653 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(208, 239, 255, 255) !important;"> Wisconsin </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 54.56411 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 48.67910 </td>
   <td style="text-align:right;background-color: rgba(208, 239, 255, 255) !important;"> 60.44912 </td>
  </tr>
</tbody>
</table>

Under this model, Harris wins all 7 key swing states in addition to taking Florida and only narrowly losing Texas. This would translate to a landslide 349-139 vote victory in the Electoral College. This said, while the bounds for these results are narrower than my previous state-level results they still show a wide range of possibilities, with all seven key swing states within the range of a Trump victory even in this model that clearly is favorable to Harris. 














