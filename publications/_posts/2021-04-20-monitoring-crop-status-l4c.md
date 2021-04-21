---
layout: post
title: Crop Condition Monitoring Using NASA's SMAP Level-4 Carbon Product
image: /assets/img/blog/GPP2017.jpg
accent_image:
  background: url('/assets/img/blog/GPP2017.jpg) center/cover
  overlay: false
accent_color: '#ccc'
theme_color: '#ccc'
description: >
 Monitoring Crop Condition at High Resolution with Remote Sensing 
sitemap: false
hide_last_modified: true
---

# Crop Condition Monitoring Using NASA's SMAP Level-4 Carbon Product

## ISSUE
Accurate monitoring of crop status over the course of the growing season is key to understanding the relationship between hydroclimatology and crop yields. 

## PROBLEM
Information on crop condition at high spatial and temporal scales over large areas has been difficult to obtain. The US Department of Agriculture (USDA) National Agricultural Statistics Service (NASS) does an excellent job of providing valuable crop data through their data portal [Quick Stats](https://quickstats.nass.usda.gov/), including weekly crop condition reports. Crop conditions are assessed by farmers and other agricultural experts in terms of the field percent observed as "Excellent", "Good", "Fair", "Poor", or "Very Poor". Detailed definitions of the crop condition categories are provided by NASS [here](https://www.nass.usda.gov/Publications/National_Crop_Progress/terms_definitions.php#condition). However, there are two major limitations in using the crop condition reports for scientific analysis:

1. The assessments are ordinal and subjective in nature, making quantitative analysis difficult.
2. The assessments are only available at the state-level, and not at county-level or finer spatial scales. The relatively rough spatial scale can be problematic in larger states with diverse climate conditions and farming practices. For example, crop conditions in Montana can vary widely between the wetter and cooler mountainous west where crops are primarily irrigated, and the dryer and warmer eastern praries where crops are primarily rain-fed. 

## SOLUTION
The first limitation was addressed by[<cite>Begauria and Maneta, 2020</cite>](https://www.pnas.org/content/117/31/18317) who transformed the ordinal data into a continuous crop condition index (CCI) that isolated the effect of natural random variability (i.e., drought, disease, etc.). For example, the effect of the [2012 drought](https://en.wikipedia.org/wiki/2012%E2%80%9313_North_American_drought) can be observed in CCI values shown in Figure 1.
<p>

{% include image.html
	    img="assets/img/blog/Begauria2020_F3.jpg"
	    title="Figure 1"
            caption="Figure 1. Crop condition index (CCI) for corn in selected states over 2012. Portions of the US corn belt suffered a severe drought over the growing season, as indicated by negative (red) CCI values. Values around zero indicate the normal condition. Figure borrowed with permission from <cite>Begauria and Maneta (2020)</cite>." %}

<p>
Recently [<cite>Jones et al. (2017)</cite>](https://ieeexplore.ieee.org/document/8008865) developed the SMAP Level-4 Carbon Product (L4C), a satellite informed model that estimates carbon exchange components including gross primary production (GPP). The project was a collaberation between NASA and the UM's Numerical Terradynamic Simulation Group [(NTSG)](https://www.ntsg.umt.edu/). Gross primary production (GPP) is a good indicator of crop condition because it captures the growth of the plant as the season progresses. The L4C is novel in that it incorporates soil moisture estimates provided by NASA's Soil Moisture Active Passive satellite (SMAP). SMAP observes microwave radiation emmitted by the Earth's surface which is sensitive to soil moisture conditions in the top 5 cm of the soil. GPP is proportional to the available soil moisture, making soil moisture an important observation when estimating GPP. Continuous soil moisture observations provided by SMAP are very useful because in-situ observations are limited by sparse point measurements. The L4C also relys on available radiation, temperature, and vapor pressure deficit. The L4C provides daily estimates at up to a 1-km resolution for different biomes like forest, grassland, and crops.

<p>
We thought that anomalies in the accumulated GPP at different stages of the growing season would be a good indicator of crop condition. If so, then the L4C could provide a measure of crop condition over the growing season at a scale of around 1-km, or about 250 acres. This is much better than crop conditions at the state-level, or even county-level.
<p>
We compared anomalies in CCI to anomalies in the total GPP over croplands within each state for two broadleaf plant types (corn and soybeans) and two cereal plant types (barley and spring wheat) to see how well the L4C indicated crop conditions at the state-level. We found that the two were significantly correlated, particularly after around 6-8 weeks after planting. 

{% include image.html
	    img="assets/img/blog/Wurster2020b_F5.jpg"
	    title="Figure 2"
            caption="Figure 2. Correlations between the state-level CCI and total accumulated GPP anomaly aggregated within the corresponding state at key stages in growth development for (A) corn, (B) soybeans, (C) barley, and (D) spring wheat. Darker greens indicate better agreement and the black dots indicate a significant correlation. Borrowed with permission from <cite>Wurster et al. (2020) </cite>"  %} 

The comparison between CCI and GPP anomalies showed that the L4C could provide information about crop condition at relatively high spatial scales (weekly), but the spatial scale remained relatively course (state-level).




























































































