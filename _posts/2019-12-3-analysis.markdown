---
layout: post
title:  "Analysis"
description: Analyzing the results.
---


# Answering the Research Questions


---
## 1. How do livestock/crops production affect different emission types (enteric fermentation, etc ..) ?
---
In this part, we will study the percentages of each crop/livestock on the different categories of emissions due to agriculture (state in Part I). FAOSTAT provides us with detailed CSV files for each type of emission. To compute the average ratio over the years, we first group for each year across all countries, sum up all emissions for each emission_type, then take the percentage of each item over its emission. 

After that, we take an average over all years to have an average ratio of emissions for each (item, emission_type) pair.

Emissions are expressed in CO2eq units.


```python
from fao_ada.correlations import compute_emissions_ratios
translation_dict = {
    "../data_cleaned/emissions_agriculture/Emissions_Agriculture_Burning_crop_residues_E_All_Data_(Normalized).csv": 72317,
    #"data_cleaned/emissions_agriculture/Emissions_Agriculture_Burning_Savanna_E_All_Data_(Normalized).csv": 72319,
    "../data_cleaned/emissions_agriculture/Emissions_Agriculture_Crop_Residues_E_All_Data_(Normalized).csv": 72312,
    #"data_cleaned/emissions_agriculture/Emissions_Agriculture_Cultivated_Organic_Soils_E_All_Data_(Normalized).csv": 72318,
    "../data_cleaned/emissions_agriculture/Emissions_Agriculture_Enteric_Fermentation_E_All_Data_(Normalized).csv":72314,
    "../data_cleaned/emissions_agriculture/Emissions_Agriculture_Manure_applied_to_soils_E_All_Data_(Normalized).csv": 72311,
    "../data_cleaned/emissions_agriculture/Emissions_Agriculture_Manure_left_on_pasture_E_All_Data_(Normalized).csv": 72310,
    "../data_cleaned/emissions_agriculture/Emissions_Agriculture_Manure_Management_E_All_Data_(Normalized).csv": 72316,
    #"data_cleaned/emissions_agriculture/Emissions_Agriculture_Synthetic_Fertilizers_E_All_Data_(Normalized).csv": 72313    
}

ratio_df = compute_emissions_ratios(translation_dict) 
```


```python
ratio_df.style.background_gradient(cmap='Reds')
```




<style  type="text/css" >
    #T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col2 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col3 {
            background-color:  #fff4ef;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col4 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col5 {
            background-color:  #fff2eb;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col1 {
            background-color:  #fcbfa7;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col1 {
            background-color:  #ffefe8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col2 {
            background-color:  #fdd1be;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col3 {
            background-color:  #fcc4ad;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col4 {
            background-color:  #fcc1a8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col5 {
            background-color:  #fee4d8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col2 {
            background-color:  #fff2ec;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col4 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col5 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col2 {
            background-color:  #fc997a;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col3 {
            background-color:  #ac1117;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col4 {
            background-color:  #dd2a25;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col5 {
            background-color:  #fdcab5;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col2 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col3 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col4 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col5 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col3 {
            background-color:  #fcbba1;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col4 {
            background-color:  #feeae0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col5 {
            background-color:  #fff0e8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col3 {
            background-color:  #fcbda4;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col4 {
            background-color:  #fee3d7;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col5 {
            background-color:  #fff0e8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col3 {
            background-color:  #ffebe2;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col4 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col5 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col2 {
            background-color:  #feeae0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col3 {
            background-color:  #ffece3;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col4 {
            background-color:  #fff0e9;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col5 {
            background-color:  #fdcbb6;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col2 {
            background-color:  #fff1ea;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col3 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col4 {
            background-color:  #fff2eb;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col5 {
            background-color:  #ffece4;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col0 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col1 {
            background-color:  #f14432;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col1 {
            background-color:  #ffece4;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col5 {
            background-color:  #fff4ef;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col1 {
            background-color:  #feeae1;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col1 {
            background-color:  #fee4d8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col0 {
            background-color:  #f03d2d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col1 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col1 {
            background-color:  #ffeee6;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col2 {
            background-color:  #fedaca;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col3 {
            background-color:  #fdc5ae;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col4 {
            background-color:  #fee8de;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col5 {
            background-color:  #fcab8f;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col1 {
            background-color:  #fee1d4;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col1 {
            background-color:  #fcc2aa;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col0 {
            background-color:  #fee9df;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col3 {
            background-color:  #fee5d8;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col4 {
            background-color:  #fee0d2;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col2 {
            background-color:  #fff2eb;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col3 {
            background-color:  #dc2924;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col4 {
            background-color:  #840711;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col3 {
            background-color:  #fee8de;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col4 {
            background-color:  #fff2ec;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col0 {
            background-color:  #ec382b;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col1 {
            background-color:  #940b13;
            color:  #f1f1f1;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }</style><table id="T_c53ae758_2197_11ea_bcdc_0c5415885990" ><thead>    <tr>        <th class="index_name level0" >element</th>        <th class="col_heading level0 col0" >Emissions (CO2eq) (Burning crop residues)</th>        <th class="col_heading level0 col1" >Emissions (CO2eq) (Crop residues)</th>        <th class="col_heading level0 col2" >Emissions (CO2eq) (Enteric)</th>        <th class="col_heading level0 col3" >Emissions (CO2eq) (Manure applied)</th>        <th class="col_heading level0 col4" >Emissions (CO2eq) (Manure management)</th>        <th class="col_heading level0 col5" >Emissions (CO2eq) (Manure on pasture)</th>    </tr>    <tr>        <th class="index_name level0" >item</th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>    </tr></thead><tbody>
                <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row0" class="row_heading level0 row0" >Asses</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col0" class="data row0 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col1" class="data row0 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col2" class="data row0 col2" >0.00543828</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col3" class="data row0 col3" >0.00128126</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col4" class="data row0 col4" >0.00253567</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row0_col5" class="data row0 col5" >0.0104046</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row1" class="row_heading level0 row1" >Barley</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col0" class="data row1 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col1" class="data row1 col1" >0.0692639</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col2" class="data row1 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col3" class="data row1 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col4" class="data row1 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row1_col5" class="data row1 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row2" class="row_heading level0 row2" >Beans, dry</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col0" class="data row2 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col1" class="data row2 col1" >0.0108659</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col2" class="data row2 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col3" class="data row2 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col4" class="data row2 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row2_col5" class="data row2 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row3" class="row_heading level0 row3" >Buffaloes</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col0" class="data row3 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col1" class="data row3 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col2" class="data row3 col2" >0.0972905</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col3" class="data row3 col3" >0.0578231</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col4" class="data row3 col4" >0.0694453</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row3_col5" class="data row3 col5" >0.0519516</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row4" class="row_heading level0 row4" >Camels</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col0" class="data row4 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col1" class="data row4 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col2" class="data row4 col2" >0.0103077</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col3" class="data row4 col3" >0.000672085</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col4" class="data row4 col4" >0.00277803</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row4_col5" class="data row4 col5" >0.00724735</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row5" class="row_heading level0 row5" >Cattle, dairy</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col0" class="data row5 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col1" class="data row5 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col2" class="data row5 col2" >0.192888</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col3" class="data row5 col3" >0.22375</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col4" class="data row5 col4" >0.20536</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row5_col5" class="data row5 col5" >0.101365</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row6" class="row_heading level0 row6" >Cattle, non-dairy</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col0" class="data row6 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col1" class="data row6 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col2" class="data row6 col2" >0.544465</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col3" class="data row6 col3" >0.263744</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col4" class="data row6 col4" >0.299471</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row6_col5" class="data row6 col5" >0.50617</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row7" class="row_heading level0 row7" >Chickens, broilers</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col0" class="data row7 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col1" class="data row7 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col2" class="data row7 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col3" class="data row7 col3" >0.0665073</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col4" class="data row7 col4" >0.020468</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row7_col5" class="data row7 col5" >0.0167826</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row8" class="row_heading level0 row8" >Chickens, layers</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col0" class="data row8 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col1" class="data row8 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col2" class="data row8 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col3" class="data row8 col3" >0.0646865</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col4" class="data row8 col4" >0.0321645</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row8_col5" class="data row8 col5" >0.0166729</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row9" class="row_heading level0 row9" >Ducks</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col0" class="data row9 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col1" class="data row9 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col2" class="data row9 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col3" class="data row9 col3" >0.0163721</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col4" class="data row9 col4" >0.00378012</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row9_col5" class="data row9 col5" >0.00562943</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row10" class="row_heading level0 row10" >Goats</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col0" class="data row10 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col1" class="data row10 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col2" class="data row10 col2" >0.0382061</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col3" class="data row10 col3" >0.0144295</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col4" class="data row10 col4" >0.00888142</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row10_col5" class="data row10 col5" >0.0993895</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row11" class="row_heading level0 row11" >Horses</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col0" class="data row11 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col1" class="data row11 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col2" class="data row11 col2" >0.0137308</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col3" class="data row11 col3" >0.00409583</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col4" class="data row11 col4" >0.00660069</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row11_col5" class="data row11 col5" >0.0269557</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row12" class="row_heading level0 row12" >Llamas</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col0" class="data row12 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col1" class="data row12 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col2" class="data row12 col2" >0.0020903</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col3" class="data row12 col3" >4.7615e-05</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col4" class="data row12 col4" >0.000468312</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row12_col5" class="data row12 col5" >0.00128571</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row13" class="row_heading level0 row13" >Maize</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col0" class="data row13 col0" >0.43026</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col1" class="data row13 col1" >0.177421</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col2" class="data row13 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col3" class="data row13 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col4" class="data row13 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row13_col5" class="data row13 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row14" class="row_heading level0 row14" >Millet</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col0" class="data row14 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col1" class="data row14 col1" >0.0150928</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col2" class="data row14 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col3" class="data row14 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col4" class="data row14 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row14_col5" class="data row14 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row15" class="row_heading level0 row15" >Mules</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col0" class="data row15 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col1" class="data row15 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col2" class="data row15 col2" >0.00176731</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col3" class="data row15 col3" >0.000380686</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col4" class="data row15 col4" >0.00077499</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row15_col5" class="data row15 col5" >0.00337372</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row16" class="row_heading level0 row16" >Oats</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col0" class="data row16 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col1" class="data row16 col1" >0.0188354</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col2" class="data row16 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col3" class="data row16 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col4" class="data row16 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row16_col5" class="data row16 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row17" class="row_heading level0 row17" >Potatoes</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col0" class="data row17 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col1" class="data row17 col1" >0.0301841</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col2" class="data row17 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col3" class="data row17 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col4" class="data row17 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row17_col5" class="data row17 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row18" class="row_heading level0 row18" >Rice, paddy</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col0" class="data row18 col0" >0.26637</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col1" class="data row18 col1" >0.295004</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col2" class="data row18 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col3" class="data row18 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col4" class="data row18 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row18_col5" class="data row18 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row19" class="row_heading level0 row19" >Rye</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col0" class="data row19 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col1" class="data row19 col1" >0.013069</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col2" class="data row19 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col3" class="data row19 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col4" class="data row19 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row19_col5" class="data row19 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row20" class="row_heading level0 row20" >Sheep</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col0" class="data row20 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col1" class="data row20 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col2" class="data row20 col2" >0.0800751</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col3" class="data row20 col3" >0.0573018</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col4" class="data row20 col4" >0.0226515</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row20_col5" class="data row20 col5" >0.151934</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row21" class="row_heading level0 row21" >Sorghum</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col0" class="data row21 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col1" class="data row21 col1" >0.0354504</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col2" class="data row21 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col3" class="data row21 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col4" class="data row21 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row21_col5" class="data row21 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row22" class="row_heading level0 row22" >Soybeans</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col0" class="data row22 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col1" class="data row22 col1" >0.0670098</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col2" class="data row22 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col3" class="data row22 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col4" class="data row22 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row22_col5" class="data row22 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row23" class="row_heading level0 row23" >Sugar cane</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col0" class="data row23 col0" >0.0310476</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col1" class="data row23 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col2" class="data row23 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col3" class="data row23 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col4" class="data row23 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row23_col5" class="data row23 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row24" class="row_heading level0 row24" >Swine, breeding</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col0" class="data row24 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col1" class="data row24 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col2" class="data row24 col2" >0.00137406</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col3" class="data row24 col3" >0.026593</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col4" class="data row24 col4" >0.0377917</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row24_col5" class="data row24 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row25" class="row_heading level0 row25" >Swine, market</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col0" class="data row25 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col1" class="data row25 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col2" class="data row25 col2" >0.0123665</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col3" class="data row25 col3" >0.181864</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col4" class="data row25 col4" >0.281389</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row25_col5" class="data row25 col5" >0</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row26" class="row_heading level0 row26" >Turkeys</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col0" class="data row26 col0" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col1" class="data row26 col1" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col2" class="data row26 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col3" class="data row26 col3" >0.0204511</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col4" class="data row26 col4" >0.00543935</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row26_col5" class="data row26 col5" >0.000837766</td>
            </tr>
            <tr>
                        <th id="T_c53ae758_2197_11ea_bcdc_0c5415885990level0_row27" class="row_heading level0 row27" >Wheat</th>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col0" class="data row27 col0" >0.272323</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col1" class="data row27 col1" >0.267804</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col2" class="data row27 col2" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col3" class="data row27 col3" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col4" class="data row27 col4" >0</td>
                        <td id="T_c53ae758_2197_11ea_bcdc_0c5415885990row27_col5" class="data row27 col5" >0</td>
            </tr>
    </tbody></table>



In columns, we have the different types of emissions of agriculture, and in rows, the ratio for each item. 
Some values are quite high, and each type of emission is dominated by one or two items:
- Emissions due to burning crop residues are largely dominated by Maize, with almost 43% of CO2eq emissions.
- Crop residues emissions are shared between Rice, Wheat and Maize, with 29%, 26%, and 17% respectivley
- Enteric fermentation is mostly just Cattle (dairy and non-dairy) with a combined 73% of Global emissions.
- Cattle are also quite highly ranked in emissions due to manure (applied to soils, management and left on pasture)

What can we conclude from this analysis ? 

It seems that Cattle is the most significant contributor in emissions of CO2eq GHG for multiple sources, with quite high percentages compared to other livestock (Chickens, goats, sheep etc..). This type of livestock is known to have a very high emission factor. Subsequently, we will study the effect of reducing the production of high emission factor items on overall emissions, using more complex models.


```python
from fao_ada.correlations import compute_emission_correlations
import warnings
emissions_agr_df_co2 = emissions_agr_df[(emissions_agr_df.elementcode == 7231) & (emissions_agr_df.year < 2020)]
warnings.filterwarnings('ignore')
correlations = compute_emission_correlations(emissions_agr_df_co2, 
                                             [livestock_df, livestock_prim_df[livestock_prim_df.elementcode == 5510], crops_df[crops_df.elementcode == 5510]])
```


```python
correlations.sort_values("correlation", ascending = False).head(15)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>itemcode_x</th>
      <th>item_x</th>
      <th>elementcode_x</th>
      <th>element_x</th>
      <th>unit_x</th>
      <th>itemcode_y</th>
      <th>item_y</th>
      <th>elementcode_y</th>
      <th>element_y</th>
      <th>unit_y</th>
      <th>correlation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1548</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.980851</td>
    </tr>
    <tr>
      <th>559</th>
      <td>5061.0</td>
      <td>Synthetic Fertilizers</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.937131</td>
    </tr>
    <tr>
      <th>1054</th>
      <td>5064.0</td>
      <td>Crop Residues</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.936495</td>
    </tr>
    <tr>
      <th>724</th>
      <td>5062.0</td>
      <td>Manure applied to Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.926835</td>
    </tr>
    <tr>
      <th>1219</th>
      <td>5066.0</td>
      <td>Burning - Crop residues</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.902941</td>
    </tr>
    <tr>
      <th>0</th>
      <td>5058.0</td>
      <td>Enteric Fermentation</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>866.0</td>
      <td>Cattle</td>
      <td>5111.0</td>
      <td>Stocks</td>
      <td>Head</td>
      <td>0.901706</td>
    </tr>
    <tr>
      <th>187</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1157.0</td>
      <td>Camelids, other</td>
      <td>5111.0</td>
      <td>Stocks</td>
      <td>Head</td>
      <td>0.875751</td>
    </tr>
    <tr>
      <th>889</th>
      <td>5063.0</td>
      <td>Manure left on Pasture</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.875106</td>
    </tr>
    <tr>
      <th>229</th>
      <td>5059.0</td>
      <td>Manure Management</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.874791</td>
    </tr>
    <tr>
      <th>634</th>
      <td>5061.0</td>
      <td>Synthetic Fertilizers</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>671.0</td>
      <td>Maté</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.835825</td>
    </tr>
    <tr>
      <th>1129</th>
      <td>5064.0</td>
      <td>Crop Residues</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>671.0</td>
      <td>Maté</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.835426</td>
    </tr>
    <tr>
      <th>1022</th>
      <td>5064.0</td>
      <td>Crop Residues</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>203.0</td>
      <td>Bambara beans</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.833105</td>
    </tr>
    <tr>
      <th>791</th>
      <td>5062.0</td>
      <td>Manure applied to Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>591.0</td>
      <td>Cashewapple</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.827823</td>
    </tr>
    <tr>
      <th>73</th>
      <td>5061.0</td>
      <td>Synthetic Fertilizers</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1157.0</td>
      <td>Camelids, other</td>
      <td>5111.0</td>
      <td>Stocks</td>
      <td>Head</td>
      <td>0.809959</td>
    </tr>
    <tr>
      <th>64</th>
      <td>5058.0</td>
      <td>Enteric Fermentation</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>305.0</td>
      <td>Tallowtree seed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>0.807329</td>
    </tr>
  </tbody>
</table>
</div>




```python
correlations.sort_values("correlation", ascending = True).head(15)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>itemcode_x</th>
      <th>item_x</th>
      <th>elementcode_x</th>
      <th>element_x</th>
      <th>unit_x</th>
      <th>itemcode_y</th>
      <th>item_y</th>
      <th>elementcode_y</th>
      <th>element_y</th>
      <th>unit_y</th>
      <th>correlation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>467</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1084.0</td>
      <td>Meat indigenous, bird nes</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.579736</td>
    </tr>
    <tr>
      <th>1604</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>554.0</td>
      <td>Cranberries</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.578395</td>
    </tr>
    <tr>
      <th>146</th>
      <td>5060.0</td>
      <td>Rice Cultivation</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1176.0</td>
      <td>Snails, not sea</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.565916</td>
    </tr>
    <tr>
      <th>1549</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>310.0</td>
      <td>Kapok fruit</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.558221</td>
    </tr>
    <tr>
      <th>131</th>
      <td>5060.0</td>
      <td>Rice Cultivation</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1111.0</td>
      <td>Meat, mule</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.540812</td>
    </tr>
    <tr>
      <th>134</th>
      <td>5060.0</td>
      <td>Rice Cultivation</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1124.0</td>
      <td>Meat indigenous, mule</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.512336</td>
    </tr>
    <tr>
      <th>483</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1151.0</td>
      <td>Meat, other rodents</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.510771</td>
    </tr>
    <tr>
      <th>484</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1154.0</td>
      <td>Meat indigenous, rodents</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.507492</td>
    </tr>
    <tr>
      <th>1642</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>789.0</td>
      <td>Sisal</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.428701</td>
    </tr>
    <tr>
      <th>186</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>1150.0</td>
      <td>Rodents, other</td>
      <td>5112.0</td>
      <td>Stocks</td>
      <td>1000 Head</td>
      <td>-0.411048</td>
    </tr>
    <tr>
      <th>1639</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>780.0</td>
      <td>Jute</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.393230</td>
    </tr>
    <tr>
      <th>1634</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>748.0</td>
      <td>Peppermint</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.382829</td>
    </tr>
    <tr>
      <th>11</th>
      <td>5058.0</td>
      <td>Enteric Fermentation</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>97.0</td>
      <td>Triticale</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.367780</td>
    </tr>
    <tr>
      <th>1509</th>
      <td>6759.0</td>
      <td>Cultivation of Organic Soils</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>161.0</td>
      <td>Sugar crops, nes</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.357870</td>
    </tr>
    <tr>
      <th>564</th>
      <td>5061.0</td>
      <td>Synthetic Fertilizers</td>
      <td>7231.0</td>
      <td>Emissions (CO2eq)</td>
      <td>Gigagrams</td>
      <td>336.0</td>
      <td>Hempseed</td>
      <td>5510.0</td>
      <td>Production</td>
      <td>tonnes</td>
      <td>-0.355365</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
