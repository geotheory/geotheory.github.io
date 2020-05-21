---
layout: post
title:  Hive plots
description: Visualising the hospitality received by Coalition Special Advisers
date:   2013-10-30 16:23:17 +0200
image: /assets/images/spad-hospitality-inv.png
header-img: /assets/images/banner-amazon.png
excerpt_separator: <!--more-->
---

With political transparency an increasingly topical subject in the wake of press scandals and allegations of official coverup, it is a useful exercise to examine any data reflecting the interaction between our leaders and our purveyors of news. Since taking power the UK coalition government has published records of hospitality received by Special Advisers – ‘Spads’ the political staff serving UK Ministers – in the line of their official duties (a longstanding requirement of civil servants). I decided to compile the various reports into a single dataset and see what insights it might offer.

<!--more-->

I have restricted the analysis to [data from the UK Cabinet Office](https://www.gov.uk/government/collections/special-advisers-transparency-publications), which has traditionally tended to function (to a degree) as an extension of the Prime Minister’s staff in 10 Downing Street. It includes Spads reporting to leaders of the Cabinet Office, Commons and Lords, and others such as Kenneth Clark designated ‘Minister without Portfolio’.

The data also includes hospitality received by the Spads appointed by Deputy Prime Minister Nick Clegg, therefore offering a small but interesting glimpse into the machinery of the Conservative/Lib Dem coalition. Clegg’s political staff account for a significant proportion of the hospitality received, which seems to support Lib Dem claims to be equal partners in the coalition. A few Spads in the registers are for reasons unknown listed as reporting variously to Clegg and to Conservative ministers at different points.

Investigating methods to visualise networks I came across [‘hive plots’](http://www.hiveplot.com/), a method devised a couple of years ago by Martin Krzywinski* to apply a simple radial structure to the data to avoid the chaos of ‘hairball’ graphics that seem to proliferate these days. Hive plots – named apparently after the shape of bee hives – group nodes according to some attribute or quality, and plot these along shared axes with their radii reflecting some other property. This is a great way to capture lots of information in addition to the relational nature of the network. See what you think (click on image to expand).

[ ![A hive plot of hospitality received by Coalition Special Advisers](/assets/images/spad-hospitality.png){:width="100%"} ](/assets/images/spad-hospitality.png)

 The first point to note is that those offering the most hospitality have been the national news media (both press and broadcast). Aside from this there are only a small number of corporate (KPMG) and other organisations hosting Spads regularly. But perhaps the most interesting aspect of the graphic is the political ordering of those giving hospitality to political staff. This does not of course necessarily reflect their political affiliations or interests, but rather the political affiliations of the Spads they have interacted with more. But since we are talking about hospitality, in each case there is certainly an agenda of one sort or another (typically information acquisition or seeking to set/influence the news agenda).

The graphic was produced in R using Bryan Hanson’s excellent _HiveR library_ which implements Krzywinski’s hive plots for R users (and my thanks to Bryan for his guidance), and annotated in Adobe Illustrator. Please get in touch if you have any queries about how it was put together.

* see **Krzywinski M, Birol I, Jones S, Marra M (2011)**. Hive Plots — Rational Approach to Visualizing Networks. Briefings in Bioinformatics

——————

Edit (25.11.13): I’ve made a demo of how to put together a hive plot with HiveR using the ggplot2 diamonds dataset – [get the code here](https://gist.github.com/geotheory/7638772).

_[Previously published at geotheory.co.uk]_
