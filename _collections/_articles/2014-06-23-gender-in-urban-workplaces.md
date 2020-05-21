---
layout: post
title:  Gender in urban workplaces
date:   2014-06-23 14:55:27 +0200
image: /assets/images/gender-density.png
header-img: /assets/images/banner-amazon.png
excerpt_separator: <!--more-->
---

In my [previous post](/articles/2014-05-30-a-new-uk-census-product-workplace-zones.html) I plotted a map of London’s workplace (biological) gender divisions, which demonstrated some interesting spatial patterns of gender distribution across the captial. I decided to replicate this to get a more representative picture of how things look across the nation (in this case England and Wales given the extent of the data, the 2011 Census published by ONS via [Nomisweb](http://www.nomisweb.co.uk/census/2011/all_tables?release=5.2a)). Here I’ve plotted the same for 28 of the principal urban centres of England and Wales. The colours are scaled by quantile according to the data distribution for the whole of England and Wales. The city maps are all plotted to a 7 km square, which enhances comparability but clips London to The City (see last for the full London map).

<!--more-->

[ ![map of gender in UK urban workplaces](/assets/images/gender-urban_workplace.png){:width="70%"} ](/assets/images/gender-urban_workplace.png)

&nbsp;

The most immediately striking observation is that workplaces in higher density urban areas seem to have higher female workforce proportions, in some cases by a quite significant margin. There also appear to be some interesting suburban clusters of both male and female dominated workplaces, particularly in larger cities (e.g. Birmingham, Manchester, Bristol). To validate the observation here is a density plot (utilising the Loess method of R’s ggplot2 package) of gender proportions by distance from these city centroids. Firstly the aggregate plot:

[ ![Aggregate gender by distance from UK urban centroids](/assets/images/gender-density.png){:width="80%"} ](/assets/images/gender-density.png)

&nbsp;

A trend of significantly more female workplaces in the central 2kms of cities is strongly supported. Plotting individual density plots for each city:

[ ![Gender by distance from UK city centres](/assets/images/gender-density-cities.png){:width="80%"} ](/assets/images/gender-density-cities.png)

&nbsp;

.. demonstrates the varied picture across England and Wales (OK.. Cardiff). The density curves corroborate the trend in many cities, with only London (strictly speaking the City) really bucking the trend.

It’s important to note that this doesn’t say anything about the types of industry that dominate these areas, or about important gender-related trends (such as pay-levels, job type and seniority) that will certainly underlie these figures. For instance some high female-proportion areas may reflect industries employing many women on lower-than-average pay, while others reflect much higher skilled professions. More analysis would need to tease these trends out.
 
##### Notes on city selection:

The cities plotted above were selected by a process that sought to identify the approximate positions of the highest density urban centres according to the data. The centre haven’t been chosen entirely arbitrarily although some arbitrary decisions did factor in the process – I aggregated the data to 1 kilometer resolution on the British National Grid, sorted it by population density and sifted out the top 28 squares that were not within 20 kms of one of higher density. This doesn’t mean these cities are the most populous or high density, but that by this data and these parameters (resolution and distance threahsold) these were found to be the highest. 20 kms was chosen to remove London’s immediate satellite towns, but it had the effect of removing Bradford for its proximity to Leeds, likewise Bath due to Bristol.

_[Previously published at geotheory.co.uk]_

