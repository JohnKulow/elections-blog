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

Insert intro writing here

## The Ground Game
### Field Offices

Insert analysis here






```
## Rows: 3113 Columns: 16
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## chr  (1): state
## dbl (11): fips, obama12fo, romney12fo, normal, medage08, pop2008, medinc08, ...
## lgl  (4): battle, swing, core_dem, core_rep
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```




<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-5-1.png" width="672" />




<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-7-1.png" width="672" />










```
## `summarise()` has grouped output by 'state'. You can override using the
## `.groups` argument.
## Scale for y is already present. Adding another scale for y, which will replace
## the existing scale.
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-8-1.png" width="672" />




<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-10-1.png" width="672" />




<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-12-1.png" width="672" />




### Campaign Events





```
## `geom_smooth()` using method = 'loess' and formula = 'y ~ x'
## `geom_smooth()` using method = 'loess' and formula = 'y ~ x'
## `geom_smooth()` using method = 'loess' and formula = 'y ~ x'
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-14-1.png" width="672" />




<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-16-1.png" width="672" />



## Updating Models
### National 2-Party Popular Vote Model



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






| Harris Vote Share| Lower Bound| Upper Bound|
|-----------------:|-----------:|-----------:|
|          52.85314|    46.85147|    58.85482|

### State 2-Party Model and Electoral College





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





Things to do:

Field Offices for 2012 and 2016
- Nationwide map
- State analysis chart
- Swing State Map

Campaign Events
- Over time graphs
- Nationwide heat map for 2016-2024
- Swing State Analysis
- State Analysis map

National 2 party vote model

State 2 party vote model/Electoral college













