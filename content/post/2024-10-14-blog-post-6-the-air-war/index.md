---
title: 'Blog Post 6: The Air War'
author: John Kulow
date: '2024-10-14'
slug: blog-post-6-the-air-war
categories: []
tags: []
---



## Introduction
Every election cycle, billions of dollars are spent on political campaigns up and down the ballot. But for all of the paid staffers, internal polls, and pricey consultants, presidential campaigns' largest expense is almost always campaign ad spending. Every year, these campaigns battle it out with their ads in the so-called "Air War," spending hundreds of millions of dollars in key swing states trying to promote themselves and destroy the reputation of their opponents. But questions remain as to how much of an effect these campaign ads actually have in these states. For this week's blog post, I will investigate this issue of campaign ad spending, looking at past trends to understand what impact ad spending will have in 2024, which is shaping up to easily be the most expensive presidential campaign in history. 

## Past Campaign Ad Spending

First, let's look at previous cycles. As you can see in the graphs below depicting how many ads were spent each day during the 2000, 2004, 2008, and 2012 campaigns, ad spending generally rises as the election progresses, with campaigns particularly ramping up their spending in the final month or two.










<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-5-1.png" width="672" />


But these graphs showing the total expenditure by each campaign on any given day do not give us the full picture. Campaign ads generally can be divided into three categories, those focused on policy issues, those focused on the candidates themselves, and those focused on both. The chart below shows us how much various campaigns spent on these different types of ads.



<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-7-1.png" width="672" />

As can be seen, candidates generally spend most of their ad spending talking about policy issues important to Americans, with the notable exception being Hillary Clinton's 2016 campaign which focused its attack ads heavily on Donald Trump's character. This said, both policy and personal types of ads can be either positive or negative.



<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-9-1.png" width="672" />


The above chart shows that between 2000 and 2012, both candidates in each race had a healthy balance of types of ads, with notable exceptions being 2008's heavy focus on contrast ads and the trend towards more negative ads in the more hostile 2012 campaign between Obama and Romney. We can also track the proportion of ads that were used to attack vs promote a candidate over time in these four campaigns:



<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-11-1.png" width="672" />


As can be seen, there is great variation between campaigns on the timing of when to attack your opponent or promote yourself. One notable moment out of these four campaigns was the anneversary of 9/11 during the 2004 campaign, at which point the campaigns switched suddenly from airing almost entirely negative ads to airing almost exclusively positive ones.








We also can trace the state-by-state expenditure over the years. 





<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-17-1.png" width="672" />




<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-19-1.png" width="672" />

As you can see in the maps above, the states that campaigns have targeted with ad spending has changed considerably over time, though certain states, such as Florida, tend to be heavily contested every cycle (although that seems likely to not be the case in 2024).

## Regression Model on Ad Spending

Knowing how much the campaigns have spent in each of the swing states every cycle and thus knowing how much of an advantage each party had in a given state, we can investigate whether these spending advantages had any impact on the election results in these states. Below are to graphs. The first depicts Democratic party spending advantage in states won or lost by less than 5 points between 2000 and 2020 (excluding 2016) compared to their two-party vote share in each said state. The second graph shows the same thing, except instead of the Democratic two-party vote share, it shows the shift towards (or against) Democrats in the two-party vote share compared to the prior election. The trendlines of each of these relationships are also shown.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-20-1.png" width="672" />

As can be seen in these two graphs, the relationship between ad spending advantage and vote share is very weak if at all present, and the relationship between spending advantage and shift in how a state votes is slightly stronger but still very weak. If I run three regression models below, a similar story plays out.

<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">Ad Spending Regression Table (2000-2020)</caption>
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="4" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">Democratic Two-Party Vote Share</th>
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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">50.18</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.22</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">49.73&nbsp;&ndash;&nbsp;50.62</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">spending diff adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.00</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.03</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.06&nbsp;&ndash;&nbsp;0.06</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.893</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">38</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.001 / -0.027</td>
</tr>

</table>
<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">Ad Spending Regression Table, w/ Vote Lag (2000-2020)</caption>
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="4" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">Democratic Two-Party Vote Share</th>
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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">46.27</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">2.85</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">40.49&nbsp;&ndash;&nbsp;52.05</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "><strong>&lt;0.001</strong></td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">spending diff adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.01</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.03</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.05&nbsp;&ndash;&nbsp;0.07</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.664</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">D pv2p lag1</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.08</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.06</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.04&nbsp;&ndash;&nbsp;0.19</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.178</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">38</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.052 / -0.002</td>
</tr>

</table>
<table style="border-collapse:collapse; border:none;">
<caption style="font-weight: bold; text-align:left;">Ad Spending Regression Table, Vote Shift (2000-2020)</caption>
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="4" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">Democratic Two-Party Vote Share Shift</th>
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
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.12</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.63</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;1.39&nbsp;&ndash;&nbsp;1.15</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.848</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">spending diff adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.12</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.08</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.05&nbsp;&ndash;&nbsp;0.29</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.160</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="4">38</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">R<sup>2</sup> / R<sup>2</sup> adjusted</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="4">0.054 / 0.028</td>
</tr>

</table>

The first of these three regression models tests the relationship between the spending difference and the Democrats' two-party popular vote share. The second model tests the same relationship, but also incorporates the prior year's election results into the model. The theory behind incorporating this data is that, for example, if there are Republican-leaning states, even if Democrats have an ad spending advantage, Republicans will likely still win the state, so correcting for historical partisan performance is important. The third model tests the relationship between spending difference and vote shift. The logic behind this model is that if Democrats spend a lot of money in a state and have an ad advantage, they might suddenly do better there, potentially explaining the shifts that swing states see from cycle to cycle.

This said, none of these three models find particularly compelling results, will particularly low R squared values in each and flat trendlines in all three.







to do's:

ad spending history (2000-2012)

2020 ad spending by state

2024 fundraising (by state, by year)

State regression on ad spending and vote share using 2000-2012 and 2020 data
^^ Add in other variables too?






