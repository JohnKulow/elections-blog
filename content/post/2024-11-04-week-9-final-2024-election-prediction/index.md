---
title: 'Week 9: Final 2024 Election Prediction'
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
Let's begin with my national popular vote prediction. For this OLS model, I used four variables:

- ***September Polling Average***: 
- ***October Polling Average***:
- ***Quarter 2 GDP Growth***:
- ***Incumbency***:









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






### Justification of Model

### Regression Table
- Include interpretation of coefficients

### Validation
- out of sample validation

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












