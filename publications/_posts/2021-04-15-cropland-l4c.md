---
layout: post
title: Crop Condition Monitoring Using NASA's SMAP Level-4 Carbon Product
image: /assets/img/blog/smap_jpl.jpg
accent_image:
  background: url('/assets/img/blog/smap_jpl.jpg) center/cover
  overlay: false
accent_color: '#ccc'
theme_color: '#ccc'
description: >
  Soil Moisture Estimated by NASA's Soil Moisture Active Passive (SMAP) Satellite Helps Provide Information on Crop Condition. Photo by NASA Jet Propulsion Laboratory.
sitemap: false
hide_last_modified: true
---
# Crop Condition Monitoring Using NASA's SMAP Level-4 Carbon Product

## Summary:
A collaboration between my research group and the Numerical Terradynamic Simulation Group (NTSG) shows that the SMAP Level-4 Carbon Product, developed by NASA and the NTSG, provides valuable information on crop conditions at higher spatial and temporal resolution than what is currently available.

## Implications:
*	**Filling in knowledge gaps:** Weekly crop condition reports available in the US are only available for individual states and is not available at the county-level. The course spatial scale may not fully capture crop conditions, particularly in larger states where crop conditions vary from place to place. Our research shows the L4C can provide information about crop condition at finer spatial scales than what is currently available. Additionally, Many countries across the world where agriculture is important do not have comprehensive data on crop condition. The L4C has the potential to fill this gap which can improve global food security.
*	**Bridging different "ways of knowing":** Farmers are experts in the cultivation of crops, and we integrate their knowledge into our scientific analysis. Integrating different "ways of knowing" like farmer knowledge and western science, is key to adapting to an uncertain future.
 
## PROBLEM
Information on crop condition at high spatial and temporal scales over large regions or continents is important for understanding the impacts of climate anomalies on agriculture. The US Department of Agriculture (USDA) National Agricultural Statistics Service (NASS) does an excellent job of providing valuable information on crop condition for the United States through their data portal [Quick Stats](https://quickstats.nass.usda.gov/). Crop conditions are assessed by farmers and other agricultural experts in terms of the field percent observed as "Excellent", "Good", "Fair", "Poor", or "Very Poor" which are provided to and reported by NASS. Detailed definitions of the crop condition categories are provided by NASS [here](https://www.nass.usda.gov/Publications/National_Crop_Progress/terms_definitions.php#condition). However, there are two major limitations in using the crop condition reports for scientific analysis:

1. The assessments are ordinal and subjective in nature (e.g., “Good” vs “Fair”), making quantitative analysis difficult.
2. The assessments are only available at the state-level, and not at county-level or finer spatial scales. The relatively rough spatial scale can be problematic in larger states with diverse climate conditions and farming practices. For example, crop conditions in Montana can vary widely between the wetter and cooler mountainous west where crops are primarily irrigated, and the dryer and warmer eastern praries where crops are primarily rain-fed. 

## SOLUTION
The first limitation was addressed by <cite>Begauria and Maneta, 2020</cite>, who transformed the ordinal data into a continuous crop condition index (CCI) that isolated the effect of natural random variability (i.e., drought, disease, etc.). For example, the effect of the [2012 drought](https://en.wikipedia.org/wiki/2012%E2%80%9313_North_American_drought) can be observed in CCI values shown in Figure 1.

![Figure1](/assets/img/blog/Begauria2020_F3.png)

Figure 1. Crop condition index (CCI) for corn in selected states over 2012. Portions of the US corn belt suffered a severe drought over the growing season, as indicated by negative (red) CCI values. Values around zero indicate the normal condition. Figure borrowed with permission from <cite>Begauria and Maneta (2020)</cite>
{:.figcaption}

Recently [<cite>Jones et al. (2017)</cite>](https://ieeexplore.ieee.org/document/8008865) developed the SMAP Level-4 Carbon Product (L4C), a satellite informed model that estimates carbon exchange components including gross primary production (GPP). The project was a collaboration between NASA and the NTSG. Gross primary production (GPP) is a good indicator of crop condition because it captures vegetation growth as the season progresses. The L4C was novel in that it incorporated soil moisture estimates provided by NASA's Soil Moisture Active Passive satellite (SMAP). SMAP observes microwave radiation emitted by the Earth's surface which is sensitive to soil moisture conditions in the top 5 cm of the soil. GPP is proportional to the available soil moisture, making soil moisture an important observation when estimating GPP. Continuous soil moisture observations provided by SMAP are very useful because in-situ observations are limited by sparse point measurements. The L4C also relies on available radiation, temperature, and vapor pressure deficit. The L4C provides daily estimates at up to a 1-km resolution for different biomes like forest, grassland, or crops.

We thought that anomalies in the accumulated GPP at different stages of the growing season would be a good indicator of crop condition. If so, then the L4C could provide a measure of crop condition over the growing season at a scale of around 1-km, or about 250 acres. This is much better than crop conditions at the state-level, or even county-level. Plus, the L4C data is available daily with global coverage.

We compared anomalies in CCI to anomalies in the total GPP over croplands within each state for two broadleaf plant types (corn and soybeans) and two cereal plant types (barley and spring wheat) to see how well the L4C indicated crop conditions at the state-level. We found that the two were significantly correlated, particularly after around 6-8 weeks after planting. 

![Figure2](/assets/img/blog/Wurster2020b_F5.png)

Figure 2. Correlations between the state-level CCI and total accumulated GPP anomaly aggregated within the corresponding state at key stages in growth development for (A) corn, (B) soybeans, (C) barley, and (D) spring wheat. Darker greens indicate better agreement and the black dots indicate a significant correlation. Borrowed with permission from <cite>Wurster et al. (2020) </cite>. 
{:.figcaption}

The comparison between CCI and GPP anomalies showed that the L4C could provide information about crop condition at relatively high temporal scales (weekly), but the spatial scale remained relatively course (state-level). So, we also used annual crop-yield data provided by NASS at the county-level, which provided the opportunity to compare the L4C to data and higher spatial resolutions, albeit at lower temporal resolution (annual as opposed to weekly). The results from the yeild analysis were similar to the comparison with CCI. Figure 3 shows the agreement between GPP anomalies and crop-yield anomalies at the county-level. 

![Figure3](/assets/img/blog/Wurster2020b_F3.png)

Figure 3. Correlations between county-level yield anomalies and county-level GPP anomalies for (A) corn and (B) soybeans at key stages of the growing season. Greener colors indicate higher positive correlations, which tend to increase as the season progresses. Soybean yield anomalies tend to be more correlated with GPP anomalies than with corn. <cite>Wurster et al. (2020)</cite>
{:.figcaption}

Our comparison between GPP anomalies estimated by the L4C and both weekly crop condition anomalies at the state-level and annual yield anomalies at the county-level showed that the SMAP L4C can provide valuable information on crop condition at higher temporal and spatial resolution that what is currently available at the time of this writing.

## Citations

Begueria, S., and Maneta, M. M. (2020). Humans as sensors: qualitative crop condition
survey data reveals spatiotemporal production patterns and allows early yield predictions.
TBDProc. Natl. Acad. USA 117, 18317–18323. doi:10.1073/pnas.1917774117.

Jones, L. A., Kimball, J. S., Reichle, R. H., Madani, N., Glassy, J., Ardizzone, J. V.,
et al. (2017). The SMAP level 4 carbon product for monitoring ecosystem land-
atmosphere CO2 exchange. IEEE Trans. Geosci. Rem. Sens. 55, 6517–6532.
doi:10.1109/TGRS.2017.2729343.

Wurster, P., Maneta, M., Kimball, J.S., Endsley, K.A., Begueria, S. (2021). Monitoring crop status in the United States using the SMAP Level-4 Carbon Product. Front. Big Data 3:597720. doi:10.3389/fdata.2020.597720.
