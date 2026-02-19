# WATREE-Annual-Tree-Cover
1. We combined machine learning and LandTrendr temporal segmentation to generate annual tree cover from 2001-2020 from the Landsat archive for Eastern Guinean Forest in Ghana and Nigerian Lowlands Forest in Nigeria.

2. Components of WATREE in Google Earth Engine
We used four scripts to generate annual impervious surface cover and developed area classification in WADISC.
1.	WATREE_1_Composites
2.	WATREE_2_Cover_RF
3.	WATREE_3_Cover_LT
These scripts are available in WATREE GEE scripts archive: https://code.earthengine.google.com/?accept_repo=users/korahandrews/WATREE
The GEE assets are configured for read-only access, and users cannot store new assets in users/korahandrews/WATREE. However, users can modify the scripts to store new assets in their GEE cloud storage.

2.1 Script #1: WATREE_1_Composites.
The first GEE script generates spectral indices, creates annual composites of indices, and exports the composites to GEE Assets or Google Drive. 

2.2. Script#2: WATREE_2_Cover_RF
The second script performs Random Forest regression using annual spectral composites and generates annual continuous tree canopy cover estimates. 

2.3 Script#3: WATREE_3_Cover_LT
The third script applies the LandTrendr algorithm (Kennedy et al., 2010) to fit a temporally segmented piecewise regression model for each pixel in the continuous tree canopy cover time series products from RF. 

# Reference
Kennedy, R. E., Yang, Z., & Cohen, W. B. (2010). Detecting trends in forest disturbance and recovery using yearly Landsat time series: 1. LandTrendr — Temporal segmentation algorithms. Remote Sensing of Environment, 114(12), 2897‐2910
