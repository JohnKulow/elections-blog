---
title: 'Blog Post 10: Post-Election Reflection'
author: John Kulow
date: '2024-11-18'
slug: blog-post-10-post-election-reflection
categories: []
tags: []
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />























## Introduction
It has now been about two weeks since the 2024 election, and, although some states like California and Alaska are still tabulating the final votes, we now have an all-but-final sense of where the national and state-level popular votes have landed. That also means that we can so how accurate, or rather how inaccurate, my predictive models were. Thus, I will begin by recapping my model and my predictions for the national popular vote, state-level results, and the electoral college, before then assessing the accuracy of my model, proposing hypotheses for my model's inaccuracies, and then suggesting ways that I could have built my model better.


## Recap of My Models and Predictions
For my predictions, I created three OLS models: one for the two-party national popular vote, one for the two-party state-level popular vote for states with public polling, and one for the two-party state-level popular vote for states *without* public polling.

### National Popular Vote
My national popular vote model included variables for the October polling average, the September polling average, the (election year) Q2 national GDP growth, and a variable for incumbency. Below was what my model predicted for Harris' two-party national vote share in the 2024 election:


| Harris Vote Share | Lower Bound | Upper Bound |
|:-----------------:|:-----------:|:-----------:|
|     51.82711      |  46.55055   |  57.10367   |

As can be seen, my model predicted incorrectly a Harris national popular vote victory, with the lower bound of the 95% confidence interval being a Trump victory with 53.45% and the upper bound being a Harris landslide with a 57.1% share of the vote.

### State-Level Vote and Electoral College
In terms of my state-level predictions, for the 23 states and two relevant congressional districts for which we had publicly available polling, I used an OLS model with variables for October and September polling averages, one- and two-cycle vote share lag, incumbent status, and the October national polling average. This model yielded the following predictions for these 25 states/districts:

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> State </th>
   <th style="text-align:center;"> Harris Vote Share </th>
   <th style="text-align:center;"> Lower Bound </th>
   <th style="text-align:center;"> Upper Bound </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> Arizona </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 50.17068 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 44.85019 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 55.49117 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(57, 114, 212, 255) !important;"> California </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 65.17024 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 59.78080 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 70.55968 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 199, 206, 255) !important;"> Florida </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 48.36540 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 43.03339 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 53.69742 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> Georgia </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 50.42399 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 45.10149 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 55.74650 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> Indiana </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 41.34649 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 36.02409 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 46.66890 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Maine Cd 2 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 46.58067 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 41.26204 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 51.89930 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(57, 114, 212, 255) !important;"> Maryland </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 68.04048 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 62.66586 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 73.41510 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(57, 114, 212, 255) !important;"> Massachusetts </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 66.76200 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 61.39923 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 72.12476 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> Michigan </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 51.44157 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 46.11853 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 56.76461 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(161, 196, 255, 255) !important;"> Minnesota </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 53.89702 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 48.57408 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 59.21996 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> Missouri </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 43.16617 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 37.83319 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 48.49915 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> Montana </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 41.09607 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 35.77414 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 46.41800 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> Nebraska </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 40.09414 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 34.76453 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 45.42374 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(161, 196, 255, 255) !important;"> Nebraska Cd 2 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 54.57686 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 49.24191 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 59.91181 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> Nevada </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 51.36874 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 46.04218 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 56.69530 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(161, 196, 255, 255) !important;"> New Hampshire </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 54.67997 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 49.34864 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 60.01130 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(161, 196, 255, 255) !important;"> New Mexico </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 54.62405 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 49.29581 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 59.95228 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(57, 114, 212, 255) !important;"> New York </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 59.86333 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 54.49855 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 65.22812 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> North Carolina </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 50.31757 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 44.98784 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 55.64730 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Ohio </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 46.02362 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 40.70049 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 51.34675 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> Pennsylvania </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 51.23316 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 45.90608 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 56.56025 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Texas </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 47.12235 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 41.80247 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 52.44224 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(161, 196, 255, 255) !important;"> Virginia </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 54.64381 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 49.32428 </td>
   <td style="text-align:center;background-color: rgba(161, 196, 255, 255) !important;"> 59.96335 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(57, 114, 212, 255) !important;"> Washington </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 60.57076 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 55.22182 </td>
   <td style="text-align:center;background-color: rgba(57, 114, 212, 255) !important;"> 65.91970 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(204, 223, 255, 255) !important;"> Wisconsin </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 51.20178 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 45.86424 </td>
   <td style="text-align:center;background-color: rgba(204, 223, 255, 255) !important;"> 56.53932 </td>
  </tr>
</tbody>
</table>

As can be seen, this model predicted a Harris victory in all seven key battleground states, with single-digit margin loses for her in Florida, Texas, Ohio, and Maine's 2nd Congressional district. The upper bounds of this model had Harris also winning these four, while the lower bounds had Trump sweeping all seven key swing states in addition to Minnesota, Nebraska's 2nd Congressional district, New Hampshire, New mexico, and Virginia.

For the remaining states for which there was no public polling, I used a similar OLS model that removed the state-level polling averages but added back in the September national polling average that the national OLS model used. Combining my state-level predictions from these two models

<img src="{{< blogdown/postref >}}index_files/figure-html/combined state pred map winner-1.png" width="672" />

This would have yielded a 319-219 electoral college victory for Harris. Clearly, however, this did not quite happen.




## Assessing My Accuracy
### National Popular Vote
As of today, the New York Times has Harris at 73,846,289 votes nationwide and Trump at 76,488,195, meaning that Harris is (currently) taking about 49.12% of the two-party national popular vote. When looking at how this compares to my national model...


| Pred. Harris % | Real Harris % | Lower Bound | Upper Bound |
|:--------------:|:-------------:|:-----------:|:-----------:|
|     51.83      |     49.12     |    46.55    |    57.1     |

... we can see that, although my model did predict a **51.83%** Harris victory that overestimate her share by **2.71%**, this margin *does* squarely fall within my 95% confidence interval, being 2.57% above my lower bound for her vote share.

### State-Level Vote and Electoral College
In terms of my state-level predictions, let's first look at my OLS model for states/districts *with* public polling. Below is the table for these 23 states and two congressional districts, shaded by how much Harris in reality underperformed my model (as seen quantified in the "Error" column).

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> State </th>
   <th style="text-align:center;"> Pred. Harris % </th>
   <th style="text-align:center;"> Real Harris % </th>
   <th style="text-align:center;"> Error </th>
   <th style="text-align:center;"> Lower Bound </th>
   <th style="text-align:left;"> Upper Bound </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> Arizona </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 50.17068 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 47.15253 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> -3.0181573 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 44.85019 </td>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> 55.49117 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: firebrick !important;"> California </td>
   <td style="text-align:center;background-color: firebrick !important;"> 65.17024 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 60.72681 </td>
   <td style="text-align:center;background-color: firebrick !important;"> -4.4434346 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 59.78080 </td>
   <td style="text-align:left;background-color: firebrick !important;"> 70.55968 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: firebrick !important;"> Florida </td>
   <td style="text-align:center;background-color: firebrick !important;"> 48.36540 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 43.37995 </td>
   <td style="text-align:center;background-color: firebrick !important;"> -4.9854536 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 43.03339 </td>
   <td style="text-align:left;background-color: firebrick !important;"> 53.69742 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Georgia </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 50.42399 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 48.87845 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.5455431 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 45.10149 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 55.74650 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Indiana </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 41.34649 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 40.34257 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.0039217 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 36.02409 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 46.66890 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Maine Cd 2 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 46.58067 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 45.37900 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.2016698 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 41.26204 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 51.89930 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: firebrick !important;"> Maryland </td>
   <td style="text-align:center;background-color: firebrick !important;"> 68.04048 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 63.31036 </td>
   <td style="text-align:center;background-color: firebrick !important;"> -4.7301230 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 62.66586 </td>
   <td style="text-align:left;background-color: firebrick !important;"> 73.41510 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: firebrick !important;"> Massachusetts </td>
   <td style="text-align:center;background-color: firebrick !important;"> 66.76200 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 62.66252 </td>
   <td style="text-align:center;background-color: firebrick !important;"> -4.0994776 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 61.39923 </td>
   <td style="text-align:left;background-color: firebrick !important;"> 72.12476 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> Michigan </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 51.44157 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 49.30156 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> -2.1400148 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 46.11853 </td>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> 56.76461 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Minnesota </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 53.89702 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 52.16725 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.7297758 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 48.57408 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 59.21996 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> Missouri </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 43.16617 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 40.64426 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> -2.5219108 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 37.83319 </td>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> 48.49915 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Montana </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 41.09607 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 39.63712 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.4589518 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 35.77414 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 46.41800 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 199, 206, 255) !important;"> Nebraska </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 40.09414 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 39.38059 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> -0.7135438 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 34.76453 </td>
   <td style="text-align:left;background-color: rgba(255, 199, 206, 255) !important;"> 45.42374 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> Nebraska Cd 2 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 54.57686 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 52.12900 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> -2.4478593 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 49.24191 </td>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> 59.91181 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> Nevada </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 51.36874 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 48.37829 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> -2.9904538 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 46.04218 </td>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> 56.69530 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> New Hampshire </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 54.67997 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 51.40987 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> -3.2701012 </td>
   <td style="text-align:center;background-color: rgba(201, 60, 76, 255) !important;"> 49.34864 </td>
   <td style="text-align:left;background-color: rgba(201, 60, 76, 255) !important;"> 60.01130 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> New Mexico </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 54.62405 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 53.00043 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.6236184 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 49.29581 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 59.95228 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: firebrick !important;"> New York </td>
   <td style="text-align:center;background-color: firebrick !important;"> 59.86333 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 55.82881 </td>
   <td style="text-align:center;background-color: firebrick !important;"> -4.0345193 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 54.49855 </td>
   <td style="text-align:left;background-color: firebrick !important;"> 65.22812 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> North Carolina </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 50.31757 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 48.29889 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> -2.0186761 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 44.98784 </td>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> 55.64730 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Ohio </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 46.02362 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 44.27299 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.7506345 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 40.70049 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 51.34675 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> Pennsylvania </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 51.23316 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 48.98235 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> -2.2508164 </td>
   <td style="text-align:center;background-color: rgba(255, 110, 126, 255) !important;"> 45.90608 </td>
   <td style="text-align:left;background-color: rgba(255, 110, 126, 255) !important;"> 56.56025 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: firebrick !important;"> Texas </td>
   <td style="text-align:center;background-color: firebrick !important;"> 47.12235 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 42.98466 </td>
   <td style="text-align:center;background-color: firebrick !important;"> -4.1376950 </td>
   <td style="text-align:center;background-color: firebrick !important;"> 41.80247 </td>
   <td style="text-align:left;background-color: firebrick !important;"> 52.44224 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Virginia </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 54.64381 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 52.85012 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.7936960 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 49.32428 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 59.96335 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 199, 206, 255) !important;"> Washington </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 60.57076 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 59.85109 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> -0.7196666 </td>
   <td style="text-align:center;background-color: rgba(255, 199, 206, 255) !important;"> 55.22182 </td>
   <td style="text-align:left;background-color: rgba(255, 199, 206, 255) !important;"> 65.91970 </td>
  </tr>
  <tr>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> Wisconsin </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 51.20178 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 49.53156 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> -1.6702249 </td>
   <td style="text-align:center;background-color: rgba(255, 158, 169, 255) !important;"> 45.86424 </td>
   <td style="text-align:left;background-color: rgba(255, 158, 169, 255) !important;"> 56.53932 </td>
  </tr>
</tbody>
</table>

In all of the above states/districts, Harris did worse than my model predicted, with larger, more diverse states such as Florida, California, Texas, and New York having the biggest misses. This said, even my most inaccurate predictions still fell within the 95% confidence interval, although some, California, Florida, and Maryland in particular, were very close, coming within a point of falling below the lower bound.

My second state-level model fared slightly better. Below is a map of how my combined predictions fared against reality, with blue-shaded states representing those which Harris did *better* than what my model(s) predicted and red-shared states being those which she did *worse* than my predictions.

<img src="{{< blogdown/postref >}}index_files/figure-html/state margin error map-1.png" width="672" />

In terms of how this translates to who actually won each state, below are the maps of the predicted and actual state-level victors (with Alaska, Hawaii, DC, and the congressional districts in Nebraska and Maine not shown, but not changing between my model compared to the results):



<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-1-1.png" width="672" />

In terms of quantifying how much my predictions were off, below are the bias, root mean squared error, and mean average error of my combined predictions:


```
## # A tibble: 1 × 3
##    Bias  RMSE   MAE
##   <dbl> <dbl> <dbl>
## 1  -1.1  2.09  1.66
```

Although less than ideal, these values are not horribly far off the final results, especially given that this race ended up being less close than 2020 (although a 1-2% error still would have substantially swung the election). This said, there were differences in how accurate my two state-level models were.

In terms of my model for states *with* polling, this model fared notably worse, with higher bias, RMSE, and MAE values compared to my overall state-level predictions:


```
## # A tibble: 1 × 3
##    bias  RMSE   MAE
##   <dbl> <dbl> <dbl>
## 1 -2.49  2.79  2.49
```

Meanwhile, the subset of states for which I used the secondary model had almost no bias, and had notably lower RMSE and MAE values:


```
## # A tibble: 1 × 3
##    bias  RMSE   MAE
##   <dbl> <dbl> <dbl>
## 1  0.02  1.24     1
```

I will explore potential reasons for this discrepancy below, but I preliminarily believe that the main reason behind this is that some of the largest shocking electoral shifts of the night happened in large, diverse states like California, New York, Texas, and Florida, all of which are important enough (either electorally or otherwise) for there to be public polling available for, whereas smaller, less diverse, electorally-safe states such as those in the Great Plains and Upper New England did not have polling.


## Potential Explanations for Inaccuracies
### Hypothesis 1: Incumbency
To begin with, I likely did not adequately consider how closely Harris would be tied to Biden in the eyes of the electorate. With the vast majority of Americans believing the country is headed in the "wrong direction" and with President Biden's approval rating being stubbornly abysmal for so long, I should have better taken into account how poorly the electorate may view the current administration, particularly as Harris repeatedly either failed or refused to distance herself from her former running mate. In fact, at one point a few weeks ago, I strongly considered adding into my model a variable for the incumbent president's (election year) June approval rating, but I decided against it because of prior beliefs that President Biden's low approval rating was driven by concerns about age that would not play into a 2024 election with Harris as the Democratic nominee and by Democrats who would vote blue come November regardless. Clearly, this was not the case, and I should not have so quickly dismissed this variable and the notable rightwards shift its inclusion would have caused in my model. This is just one way I could have adjusted my incumbency variable though, and I am sure there could have been ways to make this more nuanced, especially given how complex the "incumbency" question was this year.

### Hypothesis 2: Economics
Americans clearly are still feeling (or at least think they are feeling) the effects of inflation, and exit polls show that the economy was a top issue and that voters who cited the economy as their top issue swung towards Trump. This indicates that GDP was not an accurate indicator of how Americans were viewing the state of the economy. While this may have been a useful factor, it clearly did not capture the whole picture of how Americans have been viewing the economy. For example, I have seen numerous reports that exit polls show voters in swing states saying decisively that their local economy is doing better than four years ago, but that they perceive the *national* economy as doing worse, leading some to deem the current economic outlook in the country a "vibecession," driven by perceptions and not necessarily reality. Because of these above reasons, I could have added in variables for inflation, RDI growth, or consumer sentiment. At one point I toyed with adding in a variable for RDI growth, but I ended up not using it because historically GDP growth had been a more accurate indicator. However, I did not let that stop me from including less historically-accurate variables such as September polling averages in my model since historical accuracy does not necessarily mean that such variables do not add nuance to my model in important ways.

### Hypothesis 3: Demographics
While much more relevant to my state-level model, demographic-related electoral trends clearly played a crucial role in this election with minority voters, especially Hispanic, Asian, and Native American voters, swinging strongly towards the GOP. This has been a common explanation in the media for why states like New York, New Jersey, Illinois, California, Texas, and Florida all swung hard to the right. These demographic trends were somewhat caught preemptively by polling crosstabs, and to correct for this I could have added variables into my state-level models adjusting my polling models by trends with different demographic groups.


## How I Might Have Changed My Model
While I have proposed a number of potential changes to my model above, I would have prioritized adding in variables for RDI growth and consumer sentiment to adjust how my model defined economic perceptions, I would have prioritized adding in some demographic-related weighting mechanism for my state-level models, and I would have added back in that aforementioned June approval rating variable that I almost included in prior blog posts. While my model still likely would have missed in some ways, with the benefit of hindsight I can see why models overestimated Harris and voters' perceptions of the economy, and why my state-level model failed to adequately predict differing trends in some states and regions compared to others.

Altogether, I am fairly proud of how my model held up. While I did incorrectly predict the final result, with one or two minor adjustments the narrow victory for Harris that I predicted in the swing states easily could have shifted to being a narrow victory for Trump instead. I am also very pleased with how surprisingly well my supplementary state-level model held up, albeit with the aforementioned caveat, and I do feel that through these models and predictions I have learned more about America's electorate and what truly seems to matter in elections here.




