---
layout: post
title: Crop Condition Monitoring Using NASA's SMAP Level-4 Carbon Product
description: >
 Monitoring crop condition with remote-sensing 
sitemap: false
hide_last_modified: true
---

Accurate monitoring of crop status over the course of the growing season is key to understanding the relationship between hydroclimatology and crop yields. 

The US Department of Agriculture (USDA) National Agricultural Statistics Service (NASS) provides weekly crop condition reports through their data portal [Quick Stats](https://quickstats.nass.usda.gov/). Crop conditions are assessed by farmers and other agricultural experts in terms of the field percent observed as "Excellent", "Good", "Fair", "Poor", or "Very Poor". Detailed definitions of the crop condition categories are provided by NASS [here](https://www.nass.usda.gov/Publications/National_Crop_Progress/terms_definitions.php#condition). However, there are two major limitations in using the crop condition reports for scientific analysis:

1. The assessments are ordinal and subjective in nature, making quantitative analysis difficult.
2. The assessments are only available at the state-level, and not at county-level or finer spatial scales. The relatively rough spatial scale can be problematic in larger states with diverse climate conditions and farming practices. For example, crop conditions in Montana can vary widely between the wetter and cooler mountainous west where crops are primarily irrigated, and the dryer and warmer eastern praries where crops are primarily rain-fed. 

The first limitation was addressed by[<cite>Begauria and Maneta, 2020</cite>](https://www.pnas.org/content/117/31/18317) who transformed the ordinal data into a continuous crop condition index (CCI) that isolated the effect of natural random variability (i.e., drought, disease, etc.). For example, the effect of the [2012 drought](https://en.wikipedia.org/wiki/2012%E2%80%9313_North_American_drought) can be observed in CCI values shown in Figure 1.


{% include image.html
	    img="assets/img/blog/Begauria2020_F3.jpg"
	    title="Figure 1"
            caption="Figure 1. Crop condition index (CCI) for corn in selected states over 2012. Portions of the US corn belt suffered a severe drought over the growing season, as indicated by negative (red) CCI values. Values around zero indicate the normal condition." %}

However, CCI values remained at the state-level which may not capture variability in crop condition in larger states. 




































































































*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[JS]: JavaScript
