---
layout: post
title:  "2: Analysis"
description: Analyzing the results.
---


---
---
# Part II: Analysis
---
---

---
## 1. What are the contributions of livestock/crops for each different emission type (enteric fermentation, etc ..) ?
---
In this part, we will study the contribution of each crop/livestock on the different categories of emissions due to agriculture (stated in Part I). FAOSTAT provides us with detailed CSV files for each type of emission. To compute the average ratio over the years, we first group for each year across all countries, sum up all emissions for each emission_type, then take the percentage of each item over its emission. 

After that, we take an average over all years to have an average ratio of emissions for each (item, emission_type) pair.

Emissions are expressed in CO2eq units.

**Note**: Rice cultivation accounts for 100% of Emissions due to Rice cultivation (Eureka!)





<style  type="text/css" >
    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col2 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col3 {
            background-color:  #fff4ef;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col4 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col5 {
            background-color:  #fff2eb;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col1 {
            background-color:  #fcbfa7;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col1 {
            background-color:  #ffefe8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col2 {
            background-color:  #fdd1be;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col3 {
            background-color:  #fcc4ad;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col4 {
            background-color:  #fcc1a8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col5 {
            background-color:  #fee4d8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col2 {
            background-color:  #fff2ec;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col4 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col5 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col2 {
            background-color:  #fc997a;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col3 {
            background-color:  #ac1117;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col4 {
            background-color:  #dd2a25;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col5 {
            background-color:  #fdcab5;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col2 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col3 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col4 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col5 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col3 {
            background-color:  #fcbba1;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col4 {
            background-color:  #feeae0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col5 {
            background-color:  #fff0e8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col3 {
            background-color:  #fcbda4;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col4 {
            background-color:  #fee3d7;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col5 {
            background-color:  #fff0e8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col3 {
            background-color:  #ffebe2;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col4 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col5 {
            background-color:  #fff4ee;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col2 {
            background-color:  #feeae0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col3 {
            background-color:  #ffece3;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col4 {
            background-color:  #fff0e9;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col5 {
            background-color:  #fdcbb6;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col2 {
            background-color:  #fff1ea;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col3 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col4 {
            background-color:  #fff2eb;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col5 {
            background-color:  #ffece4;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col0 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col1 {
            background-color:  #f14432;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col1 {
            background-color:  #ffece4;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col5 {
            background-color:  #fff4ef;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col1 {
            background-color:  #feeae1;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col1 {
            background-color:  #fee4d8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col0 {
            background-color:  #f03d2d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col1 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col6 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col1 {
            background-color:  #ffeee6;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col2 {
            background-color:  #fedaca;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col3 {
            background-color:  #fdc5ae;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col4 {
            background-color:  #fee8de;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col5 {
            background-color:  #fcab8f;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col1 {
            background-color:  #fee1d4;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col1 {
            background-color:  #fcc2aa;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col0 {
            background-color:  #fee9df;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col3 {
            background-color:  #fee5d8;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col4 {
            background-color:  #fee0d2;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col2 {
            background-color:  #fff2eb;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col3 {
            background-color:  #dc2924;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col4 {
            background-color:  #840711;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col3 {
            background-color:  #fee8de;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col4 {
            background-color:  #fff2ec;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col0 {
            background-color:  #ec382b;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col1 {
            background-color:  #940b13;
            color:  #f1f1f1;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col4 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col5 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col6 {
            background-color:  #fff5f0;
            color:  #000000;
        }</style><table id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3e" ><thead>    <tr>        <th class="index_name level0" >element</th>        <th class="col_heading level0 col0" >Emissions (CO2eq) (Burning crop residues)</th>        <th class="col_heading level0 col1" >Emissions (CO2eq) (Crop residues)</th>        <th class="col_heading level0 col2" >Emissions (CO2eq) (Enteric)</th>        <th class="col_heading level0 col3" >Emissions (CO2eq) (Manure applied)</th>        <th class="col_heading level0 col4" >Emissions (CO2eq) (Manure management)</th>        <th class="col_heading level0 col5" >Emissions (CO2eq) (Manure on pasture)</th>        <th class="col_heading level0 col6" >Emissions (CO2eq) (Rice cultivation)</th>    </tr>    <tr>        <th class="index_name level0" >item</th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>    </tr></thead><tbody>
                <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row0" class="row_heading level0 row0" >Asses</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col0" class="data row0 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col1" class="data row0 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col2" class="data row0 col2" >0.00543828</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col3" class="data row0 col3" >0.00128126</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col4" class="data row0 col4" >0.00253567</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col5" class="data row0 col5" >0.0104046</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow0_col6" class="data row0 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row1" class="row_heading level0 row1" >Barley</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col0" class="data row1 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col1" class="data row1 col1" >0.0692639</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col2" class="data row1 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col3" class="data row1 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col4" class="data row1 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col5" class="data row1 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow1_col6" class="data row1 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row2" class="row_heading level0 row2" >Beans, dry</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col0" class="data row2 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col1" class="data row2 col1" >0.0108659</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col2" class="data row2 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col3" class="data row2 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col4" class="data row2 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col5" class="data row2 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow2_col6" class="data row2 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row3" class="row_heading level0 row3" >Buffaloes</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col0" class="data row3 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col1" class="data row3 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col2" class="data row3 col2" >0.0972905</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col3" class="data row3 col3" >0.0578231</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col4" class="data row3 col4" >0.0694453</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col5" class="data row3 col5" >0.0519516</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow3_col6" class="data row3 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row4" class="row_heading level0 row4" >Camels</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col0" class="data row4 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col1" class="data row4 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col2" class="data row4 col2" >0.0103077</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col3" class="data row4 col3" >0.000672085</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col4" class="data row4 col4" >0.00277803</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col5" class="data row4 col5" >0.00724735</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow4_col6" class="data row4 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row5" class="row_heading level0 row5" >Cattle, dairy</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col0" class="data row5 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col1" class="data row5 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col2" class="data row5 col2" >0.192888</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col3" class="data row5 col3" >0.22375</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col4" class="data row5 col4" >0.20536</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col5" class="data row5 col5" >0.101365</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow5_col6" class="data row5 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row6" class="row_heading level0 row6" >Cattle, non-dairy</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col0" class="data row6 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col1" class="data row6 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col2" class="data row6 col2" >0.544465</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col3" class="data row6 col3" >0.263744</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col4" class="data row6 col4" >0.299471</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col5" class="data row6 col5" >0.50617</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow6_col6" class="data row6 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row7" class="row_heading level0 row7" >Chickens, broilers</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col0" class="data row7 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col1" class="data row7 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col2" class="data row7 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col3" class="data row7 col3" >0.0665073</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col4" class="data row7 col4" >0.020468</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col5" class="data row7 col5" >0.0167826</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow7_col6" class="data row7 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row8" class="row_heading level0 row8" >Chickens, layers</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col0" class="data row8 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col1" class="data row8 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col2" class="data row8 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col3" class="data row8 col3" >0.0646865</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col4" class="data row8 col4" >0.0321645</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col5" class="data row8 col5" >0.0166729</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow8_col6" class="data row8 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row9" class="row_heading level0 row9" >Ducks</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col0" class="data row9 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col1" class="data row9 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col2" class="data row9 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col3" class="data row9 col3" >0.0163721</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col4" class="data row9 col4" >0.00378012</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col5" class="data row9 col5" >0.00562943</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow9_col6" class="data row9 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row10" class="row_heading level0 row10" >Goats</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col0" class="data row10 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col1" class="data row10 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col2" class="data row10 col2" >0.0382061</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col3" class="data row10 col3" >0.0144295</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col4" class="data row10 col4" >0.00888142</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col5" class="data row10 col5" >0.0993895</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow10_col6" class="data row10 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row11" class="row_heading level0 row11" >Horses</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col0" class="data row11 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col1" class="data row11 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col2" class="data row11 col2" >0.0137308</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col3" class="data row11 col3" >0.00409583</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col4" class="data row11 col4" >0.00660069</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col5" class="data row11 col5" >0.0269557</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow11_col6" class="data row11 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row12" class="row_heading level0 row12" >Llamas</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col0" class="data row12 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col1" class="data row12 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col2" class="data row12 col2" >0.0020903</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col3" class="data row12 col3" >4.7615e-05</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col4" class="data row12 col4" >0.000468312</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col5" class="data row12 col5" >0.00128571</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow12_col6" class="data row12 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row13" class="row_heading level0 row13" >Maize</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col0" class="data row13 col0" >0.43026</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col1" class="data row13 col1" >0.177421</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col2" class="data row13 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col3" class="data row13 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col4" class="data row13 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col5" class="data row13 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow13_col6" class="data row13 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row14" class="row_heading level0 row14" >Millet</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col0" class="data row14 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col1" class="data row14 col1" >0.0150928</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col2" class="data row14 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col3" class="data row14 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col4" class="data row14 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col5" class="data row14 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow14_col6" class="data row14 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row15" class="row_heading level0 row15" >Mules</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col0" class="data row15 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col1" class="data row15 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col2" class="data row15 col2" >0.00176731</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col3" class="data row15 col3" >0.000380686</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col4" class="data row15 col4" >0.00077499</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col5" class="data row15 col5" >0.00337372</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow15_col6" class="data row15 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row16" class="row_heading level0 row16" >Oats</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col0" class="data row16 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col1" class="data row16 col1" >0.0188354</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col2" class="data row16 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col3" class="data row16 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col4" class="data row16 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col5" class="data row16 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow16_col6" class="data row16 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row17" class="row_heading level0 row17" >Potatoes</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col0" class="data row17 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col1" class="data row17 col1" >0.0301841</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col2" class="data row17 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col3" class="data row17 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col4" class="data row17 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col5" class="data row17 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow17_col6" class="data row17 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row18" class="row_heading level0 row18" >Rice, paddy</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col0" class="data row18 col0" >0.26637</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col1" class="data row18 col1" >0.295004</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col2" class="data row18 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col3" class="data row18 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col4" class="data row18 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col5" class="data row18 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow18_col6" class="data row18 col6" >1</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row19" class="row_heading level0 row19" >Rye</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col0" class="data row19 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col1" class="data row19 col1" >0.013069</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col2" class="data row19 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col3" class="data row19 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col4" class="data row19 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col5" class="data row19 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow19_col6" class="data row19 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row20" class="row_heading level0 row20" >Sheep</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col0" class="data row20 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col1" class="data row20 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col2" class="data row20 col2" >0.0800751</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col3" class="data row20 col3" >0.0573018</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col4" class="data row20 col4" >0.0226515</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col5" class="data row20 col5" >0.151934</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow20_col6" class="data row20 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row21" class="row_heading level0 row21" >Sorghum</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col0" class="data row21 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col1" class="data row21 col1" >0.0354504</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col2" class="data row21 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col3" class="data row21 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col4" class="data row21 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col5" class="data row21 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow21_col6" class="data row21 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row22" class="row_heading level0 row22" >Soybeans</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col0" class="data row22 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col1" class="data row22 col1" >0.0670098</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col2" class="data row22 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col3" class="data row22 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col4" class="data row22 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col5" class="data row22 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow22_col6" class="data row22 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row23" class="row_heading level0 row23" >Sugar cane</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col0" class="data row23 col0" >0.0310476</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col1" class="data row23 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col2" class="data row23 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col3" class="data row23 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col4" class="data row23 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col5" class="data row23 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow23_col6" class="data row23 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row24" class="row_heading level0 row24" >Swine, breeding</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col0" class="data row24 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col1" class="data row24 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col2" class="data row24 col2" >0.00137406</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col3" class="data row24 col3" >0.026593</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col4" class="data row24 col4" >0.0377917</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col5" class="data row24 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow24_col6" class="data row24 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row25" class="row_heading level0 row25" >Swine, market</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col0" class="data row25 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col1" class="data row25 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col2" class="data row25 col2" >0.0123665</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col3" class="data row25 col3" >0.181864</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col4" class="data row25 col4" >0.281389</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col5" class="data row25 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow25_col6" class="data row25 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row26" class="row_heading level0 row26" >Turkeys</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col0" class="data row26 col0" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col1" class="data row26 col1" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col2" class="data row26 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col3" class="data row26 col3" >0.0204511</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col4" class="data row26 col4" >0.00543935</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col5" class="data row26 col5" >0.000837766</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow26_col6" class="data row26 col6" >0</td>
            </tr>
            <tr>
                        <th id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3elevel0_row27" class="row_heading level0 row27" >Wheat</th>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col0" class="data row27 col0" >0.272323</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col1" class="data row27 col1" >0.267804</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col2" class="data row27 col2" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col3" class="data row27 col3" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col4" class="data row27 col4" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col5" class="data row27 col5" >0</td>
                        <td id="T_741539aa_2306_11ea_8a32_cda3d6ffcd3erow27_col6" class="data row27 col6" >0</td>
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

---
## 2. Have emissions increased proportionally to production ?
---
In this question, we will study whether emissions and production of different items are have increased proportionally over time. To come up with such metric, we will need to study the emissions per head of livestock animal, and per hectar of cultivated soil.

If it is the case, we should see no increase in this ratio. Let's work this out


![png](assets/img/output_76_0.png)


The graph looks nice and straight: Emission factors by Gigagram / head for live animals has not increased or decreased, and the same goes for rice cultivation.

We were not able to obtain an emission factor for various other crops, as the data is not available and trying to reconstruct it would introduce a lot of error margin, which is why we decided to stick with what we have.

The above graphs allows us to conclude the following:

Emissions have only increased due to the increase in production, and is not due to other factors such as different growing or breeding techniques.

---
## 3. Which product's production should be reduced as to reduce emissions ?
---

In this part, we aim at quantifying the linear relationships between all productions we have (233 different items) and all types of emissions (10 type) that are due to agriculture.

In order to do that, we first compute each pair of production and emission's correlation over the years using Pearson's Correlation Coefficient for every country, and then average the correlation over all the countries.

This yields a dataframe with 2330 correlation coefficients (a bit less due to data inconsistency). These will be useful later on when we will want to build regressive models that estimate different emissions based on production items.

We will study the correlations for Live animals, Livestock produce and Crops independantly


### 3.1. Live animals
---
From the previous anylsis, we know that live animals only contribute to 4 types of emissions: Enteric fermentation, Manure Mangement, Manure applied to soils and Manure left on pasture. For this reason, we will only take into account correlations with these emission types, as even if we have large correlations with other types, we know they do not apply.







<style  type="text/css" >
    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col1 {
            background-color:  #d82422;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col2 {
            background-color:  #db2824;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col0 {
            background-color:  #fcc2aa;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col1 {
            background-color:  #fdcdb9;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col2 {
            background-color:  #fdcab5;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col3 {
            background-color:  #fcaf93;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col0 {
            background-color:  #fc8b6b;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col1 {
            background-color:  #fb6c4c;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col2 {
            background-color:  #f6583e;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col3 {
            background-color:  #fb7c5c;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col0 {
            background-color:  #fa6849;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col1 {
            background-color:  #fc9474;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col2 {
            background-color:  #fca588;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col3 {
            background-color:  #fc8060;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col0 {
            background-color:  #9c0d14;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col1 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col2 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col3 {
            background-color:  #6f020e;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col0 {
            background-color:  #fb7555;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col1 {
            background-color:  #fb7555;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col2 {
            background-color:  #fc7f5f;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col3 {
            background-color:  #fb6b4b;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col0 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col1 {
            background-color:  #a91016;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col2 {
            background-color:  #ac1117;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col3 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col0 {
            background-color:  #fb6d4d;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col1 {
            background-color:  #c5171c;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col2 {
            background-color:  #9c0d14;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col3 {
            background-color:  #e53228;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col0 {
            background-color:  #fc9b7c;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col1 {
            background-color:  #f85f43;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col2 {
            background-color:  #ee3a2c;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col3 {
            background-color:  #fa6849;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col0 {
            background-color:  #fca082;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col1 {
            background-color:  #fc8f6f;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col2 {
            background-color:  #fb7858;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col3 {
            background-color:  #fb7b5b;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col0 {
            background-color:  #fb7252;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col1 {
            background-color:  #f6563d;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col2 {
            background-color:  #f5533b;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col3 {
            background-color:  #ec382b;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col0 {
            background-color:  #fdc6b0;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col1 {
            background-color:  #fdcbb6;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col2 {
            background-color:  #fdcbb6;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col3 {
            background-color:  #fca588;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col0 {
            background-color:  #fee5d9;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col3 {
            background-color:  #fedfd0;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col0 {
            background-color:  #fcb79c;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col1 {
            background-color:  #fb7a5a;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col2 {
            background-color:  #fb7858;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col3 {
            background-color:  #fca689;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col0 {
            background-color:  #fb7252;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col1 {
            background-color:  #9f0e14;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col2 {
            background-color:  #b11218;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col3 {
            background-color:  #f85f43;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col0 {
            background-color:  #fc9777;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col1 {
            background-color:  #fc8565;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col2 {
            background-color:  #fb7555;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col3 {
            background-color:  #fc9373;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col0 {
            background-color:  #ffede5;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col1 {
            background-color:  #fee7dc;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col2 {
            background-color:  #fdcebb;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col3 {
            background-color:  #ffebe2;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col0 {
            background-color:  #f24734;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col1 {
            background-color:  #f44d38;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col2 {
            background-color:  #f34c37;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col3 {
            background-color:  #ca181d;
            color:  #f1f1f1;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col0 {
            background-color:  #fcc3ab;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col1 {
            background-color:  #fc9b7c;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col2 {
            background-color:  #fb7252;
            color:  #000000;
        }    #T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col3 {
            background-color:  #fcb89e;
            color:  #000000;
        }</style><table id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3e" ><thead>    <tr>        <th class="index_name level0" >item_x</th>        <th class="col_heading level0 col0" >Enteric Fermentation</th>        <th class="col_heading level0 col1" >Manure Management</th>        <th class="col_heading level0 col2" >Manure applied to Soils</th>        <th class="col_heading level0 col3" >Manure left on Pasture</th>    </tr>    <tr>        <th class="index_name level0" >item_y</th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>    </tr></thead><tbody>
                <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row0" class="row_heading level0 row0" >Animals live nes</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col0" class="data row0 col0" >-0.0174319</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col1" class="data row0 col1" >0.559531</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col2" class="data row0 col2" >0.530239</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow0_col3" class="data row0 col3" >-0.0536317</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row1" class="row_heading level0 row1" >Asses</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col0" class="data row1 col0" >0.192255</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col1" class="data row1 col1" >0.140286</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col2" class="data row1 col2" >0.119927</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow1_col3" class="data row1 col3" >0.193451</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row2" class="row_heading level0 row2" >Beehives</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col0" class="data row2 col0" >0.348389</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col1" class="data row2 col1" >0.386578</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col2" class="data row2 col2" >0.408019</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow2_col3" class="data row2 col3" >0.324757</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row3" class="row_heading level0 row3" >Buffaloes</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col0" class="data row3 col0" >0.447421</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col1" class="data row3 col1" >0.284779</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col2" class="data row3 col2" >0.217855</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow3_col3" class="data row3 col3" >0.316874</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row4" class="row_heading level0 row4" >Camelids, other</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col0" class="data row4 col0" >0.801259</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col1" class="data row4 col1" >0.801915</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col2" class="data row4 col2" >0.78622</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow4_col3" class="data row4 col3" >0.788628</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row5" class="row_heading level0 row5" >Camels</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col0" class="data row5 col0" >0.412462</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col1" class="data row5 col1" >0.366456</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col2" class="data row5 col2" >0.315086</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow5_col3" class="data row5 col3" >0.373481</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row6" class="row_heading level0 row6" >Cattle</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col0" class="data row6 col0" >0.901706</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col1" class="data row6 col1" >0.689737</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col2" class="data row6 col2" >0.661271</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow6_col3" class="data row6 col3" >0.80322</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row7" class="row_heading level0 row7" >Chickens</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col0" class="data row7 col0" >0.431695</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col1" class="data row7 col1" >0.610417</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col2" class="data row7 col2" >0.696948</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow7_col3" class="data row7 col3" >0.511537</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row8" class="row_heading level0 row8" >Ducks</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col0" class="data row8 col0" >0.305179</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col1" class="data row8 col1" >0.417602</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col2" class="data row8 col2" >0.47472</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow8_col3" class="data row8 col3" >0.380987</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row9" class="row_heading level0 row9" >Geese and guinea fowls</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col0" class="data row9 col0" >0.289634</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col1" class="data row9 col1" >0.299573</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col2" class="data row9 col2" >0.332088</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow9_col3" class="data row9 col3" >0.328897</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row10" class="row_heading level0 row10" >Goats</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col0" class="data row10 col0" >0.417793</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col1" class="data row10 col1" >0.435975</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col2" class="data row10 col2" >0.41988</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow10_col3" class="data row10 col3" >0.490726</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row11" class="row_heading level0 row11" >Horses</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col0" class="data row11 col0" >0.179563</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col1" class="data row11 col1" >0.146376</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col2" class="data row11 col2" >0.115398</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow11_col3" class="data row11 col3" >0.219399</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row12" class="row_heading level0 row12" >Mules</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col0" class="data row12 col0" >0.0719545</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col1" class="data row12 col1" >-0.0160093</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col2" class="data row12 col2" >-0.0486916</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow12_col3" class="data row12 col3" >0.0582932</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row13" class="row_heading level0 row13" >Pigeons, other birds</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col0" class="data row13 col0" >0.224025</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col1" class="data row13 col1" >0.352663</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col2" class="data row13 col2" >0.329942</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow13_col3" class="data row13 col3" >0.217039</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row14" class="row_heading level0 row14" >Pigs</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col0" class="data row14 col0" >0.417244</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col1" class="data row14 col1" >0.706259</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col2" class="data row14 col2" >0.64776</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow14_col3" class="data row14 col3" >0.400493</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row15" class="row_heading level0 row15" >Rabbits and hares</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col0" class="data row15 col0" >0.316292</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col1" class="data row15 col1" >0.322828</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col2" class="data row15 col2" >0.341396</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow15_col3" class="data row15 col3" >0.264436</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row16" class="row_heading level0 row16" >Rodents, other</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col0" class="data row16 col0" >0.0281794</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col1" class="data row16 col1" >0.0519693</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col2" class="data row16 col2" >0.104789</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow16_col3" class="data row16 col3" >-0.00175626</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row17" class="row_heading level0 row17" >Sheep</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col0" class="data row17 col0" >0.525571</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col1" class="data row17 col1" >0.454382</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col2" class="data row17 col2" >0.43425</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow17_col3" class="data row17 col3" >0.591585</td>
            </tr>
            <tr>
                        <th id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3elevel0_row18" class="row_heading level0 row18" >Turkeys</th>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col0" class="data row18 col0" >0.190052</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col1" class="data row18 col1" >0.270763</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col2" class="data row18 col2" >0.348869</td>
                        <td id="T_83921c36_2306_11ea_8a32_cda3d6ffcd3erow18_col3" class="data row18 col3" >0.16829</td>
            </tr>
    </tbody></table>



The results are coherent with the previous calculations based on contributions:
- Cattle has a high correlation coefficient with all 4 emission types, and most with enteric fermentation. We previously saw that Cattle (dairy and non-dairy) account for almost 75% of this type of emission. Also, in the begining of our study, we showed that Enteric Fermentation accounts for 67% of CH4 Emissons of this economy. Simple calculations yield a global contribution to CH4 gases of 50% for Cattle !!
- Camelids seem to also have a high coefficient with the 4 emission types, but we previously saw that they only account for 1% of emissions.
- Mules have the lowest correlations with all 4 types.


### 3.2. Livestock Produce
---





<style  type="text/css" >
    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col0 {
            background-color:  #ef3c2c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col1 {
            background-color:  #b61319;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col2 {
            background-color:  #880811;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col3 {
            background-color:  #e43027;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col0 {
            background-color:  #fb7252;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col1 {
            background-color:  #f34a36;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col2 {
            background-color:  #d01d1f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col3 {
            background-color:  #f6553c;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col0 {
            background-color:  #c5171c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col1 {
            background-color:  #f34a36;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col2 {
            background-color:  #ec382b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col3 {
            background-color:  #ed392b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col0 {
            background-color:  #7a0510;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col1 {
            background-color:  #b51318;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col2 {
            background-color:  #9d0d14;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col3 {
            background-color:  #b01217;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col0 {
            background-color:  #8e0912;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col1 {
            background-color:  #940b13;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col2 {
            background-color:  #840711;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col3 {
            background-color:  #8c0912;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col0 {
            background-color:  #f03f2e;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col1 {
            background-color:  #d32020;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col2 {
            background-color:  #bc141a;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col3 {
            background-color:  #f5523a;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col0 {
            background-color:  #c1161b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col1 {
            background-color:  #f24734;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col2 {
            background-color:  #ec382b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col3 {
            background-color:  #e43027;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col0 {
            background-color:  #ce1a1e;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col1 {
            background-color:  #d52221;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col2 {
            background-color:  #c7171c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col3 {
            background-color:  #e63328;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col0 {
            background-color:  #77040f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col1 {
            background-color:  #af1117;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col2 {
            background-color:  #960b13;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col3 {
            background-color:  #b01217;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col0 {
            background-color:  #fa6648;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col1 {
            background-color:  #c8171c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col2 {
            background-color:  #960b13;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col3 {
            background-color:  #f24633;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col0 {
            background-color:  #fb7d5d;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col1 {
            background-color:  #e93529;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col2 {
            background-color:  #b81419;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col3 {
            background-color:  #f85d42;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col0 {
            background-color:  #fc7f5f;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col1 {
            background-color:  #fb7b5b;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col2 {
            background-color:  #e22e27;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col3 {
            background-color:  #f6553c;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col0 {
            background-color:  #ed392b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col1 {
            background-color:  #dc2924;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col2 {
            background-color:  #bf151b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col3 {
            background-color:  #d92523;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col0 {
            background-color:  #fc9879;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col1 {
            background-color:  #fcb69b;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col2 {
            background-color:  #fb7151;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col3 {
            background-color:  #fca78b;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col0 {
            background-color:  #f34c37;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col1 {
            background-color:  #fa6547;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col2 {
            background-color:  #e22e27;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col3 {
            background-color:  #da2723;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col0 {
            background-color:  #fca285;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col1 {
            background-color:  #fdcbb6;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col2 {
            background-color:  #fc8d6d;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col3 {
            background-color:  #fc8f6f;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col0 {
            background-color:  #f34c37;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col1 {
            background-color:  #9c0d14;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col2 {
            background-color:  #8c0912;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col3 {
            background-color:  #f34c37;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col0 {
            background-color:  #de2b25;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col1 {
            background-color:  #de2b25;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col2 {
            background-color:  #be151a;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col3 {
            background-color:  #f03f2e;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col0 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col2 {
            background-color:  #fc9777;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col0 {
            background-color:  #e02c26;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col1 {
            background-color:  #e02c26;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col2 {
            background-color:  #c3161b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col3 {
            background-color:  #d52221;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col0 {
            background-color:  #fedccd;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col1 {
            background-color:  #fdc6b0;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col2 {
            background-color:  #f6583e;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col3 {
            background-color:  #fed9c9;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col0 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col1 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col2 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col3 {
            background-color:  #67000d;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col0 {
            background-color:  #f14331;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col1 {
            background-color:  #f03d2d;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col2 {
            background-color:  #d11e1f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col3 {
            background-color:  #f5533b;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col0 {
            background-color:  #9d0d14;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col1 {
            background-color:  #ea362a;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col2 {
            background-color:  #e12d26;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col3 {
            background-color:  #dd2a25;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col0 {
            background-color:  #a91016;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col1 {
            background-color:  #a91016;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col2 {
            background-color:  #ab1016;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col3 {
            background-color:  #bf151b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col0 {
            background-color:  #920a13;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col1 {
            background-color:  #b61319;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col2 {
            background-color:  #9c0d14;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col3 {
            background-color:  #b31218;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col0 {
            background-color:  #fb6c4c;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col1 {
            background-color:  #cb181d;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col2 {
            background-color:  #9c0d14;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col3 {
            background-color:  #f34a36;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col0 {
            background-color:  #fc8767;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col1 {
            background-color:  #f34a36;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col2 {
            background-color:  #c4161c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col3 {
            background-color:  #fb7151;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col0 {
            background-color:  #f34935;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col1 {
            background-color:  #d21f20;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col2 {
            background-color:  #b21218;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col3 {
            background-color:  #f34c37;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col0 {
            background-color:  #f5523a;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col1 {
            background-color:  #f14432;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col2 {
            background-color:  #d21f20;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col3 {
            background-color:  #ed392b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col0 {
            background-color:  #fb7252;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col1 {
            background-color:  #fa6849;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col2 {
            background-color:  #d52221;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col3 {
            background-color:  #f44d38;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col0 {
            background-color:  #fc9373;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col1 {
            background-color:  #fcbda4;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col2 {
            background-color:  #fb7656;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col3 {
            background-color:  #fc9070;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col0 {
            background-color:  #f5523a;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col1 {
            background-color:  #fb6c4c;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col2 {
            background-color:  #e93529;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col3 {
            background-color:  #dd2a25;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col0 {
            background-color:  #fc8767;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col1 {
            background-color:  #fb7b5b;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col2 {
            background-color:  #e53228;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col3 {
            background-color:  #fc8262;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col0 {
            background-color:  #e63328;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col1 {
            background-color:  #f44d38;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col2 {
            background-color:  #dc2924;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col3 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col0 {
            background-color:  #fff2ec;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col1 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col2 {
            background-color:  #fc9777;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col3 {
            background-color:  #fff3ed;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col0 {
            background-color:  #f5533b;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col1 {
            background-color:  #a10e15;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col2 {
            background-color:  #940b13;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col3 {
            background-color:  #f6553c;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col0 {
            background-color:  #f14331;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col1 {
            background-color:  #f24633;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col2 {
            background-color:  #cf1c1f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col3 {
            background-color:  #f85d42;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col0 {
            background-color:  #dc2924;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col1 {
            background-color:  #e22e27;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col2 {
            background-color:  #c5171c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col3 {
            background-color:  #d72322;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col0 {
            background-color:  #fee6da;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col1 {
            background-color:  #fdc6b0;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col2 {
            background-color:  #f7593f;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col3 {
            background-color:  #fee0d2;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col0 {
            background-color:  #f44f39;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col1 {
            background-color:  #f24734;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col2 {
            background-color:  #e12d26;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col3 {
            background-color:  #f14331;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col0 {
            background-color:  #a60f15;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col1 {
            background-color:  #af1117;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col2 {
            background-color:  #aa1016;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col3 {
            background-color:  #bb141a;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col0 {
            background-color:  #aa1016;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col1 {
            background-color:  #9f0e14;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col2 {
            background-color:  #75030f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col3 {
            background-color:  #be151a;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col0 {
            background-color:  #e93529;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col1 {
            background-color:  #e83429;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col2 {
            background-color:  #ce1a1e;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col3 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col0 {
            background-color:  #d11e1f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col1 {
            background-color:  #d92523;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col2 {
            background-color:  #bd151a;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col3 {
            background-color:  #c2161b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col0 {
            background-color:  #f14130;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col1 {
            background-color:  #e43027;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col2 {
            background-color:  #c8171c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col3 {
            background-color:  #e43027;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col0 {
            background-color:  #da2723;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col1 {
            background-color:  #e12d26;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col2 {
            background-color:  #c7171c;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col3 {
            background-color:  #cf1c1f;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col0 {
            background-color:  #f34c37;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col1 {
            background-color:  #f5523a;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col2 {
            background-color:  #da2723;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col3 {
            background-color:  #e43027;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col0 {
            background-color:  #c3161b;
            color:  #f1f1f1;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col1 {
            background-color:  #fb7353;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col3 {
            background-color:  #f03d2d;
            color:  #f1f1f1;
        }</style><table id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3e" ><thead>    <tr>        <th class="index_name level0" >item_x</th>        <th class="col_heading level0 col0" >Enteric Fermentation</th>        <th class="col_heading level0 col1" >Manure Management</th>        <th class="col_heading level0 col2" >Manure applied to Soils</th>        <th class="col_heading level0 col3" >Manure left on Pasture</th>    </tr>    <tr>        <th class="index_name level0" >item_y</th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>        <th class="blank" ></th>    </tr></thead><tbody>
                <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row0" class="row_heading level0 row0" >Eggs, hen, in shell</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col0" class="data row0 col0" >0.412908</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col1" class="data row0 col1" >0.545695</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col2" class="data row0 col2" >0.604489</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow0_col3" class="data row0 col3" >0.465691</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row1" class="row_heading level0 row1" >Eggs, other bird, in shell</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col0" class="data row1 col0" >0.309624</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col1" class="data row1 col1" >0.389675</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col2" class="data row1 col2" >0.412316</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow1_col3" class="data row1 col3" >0.388253</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row2" class="row_heading level0 row2" >Hides, buffalo, fresh</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col0" class="data row2 col0" >0.51327</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col1" class="data row2 col1" >0.388345</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col2" class="data row2 col2" >0.317292</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow2_col3" class="data row2 col3" >0.443552</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row3" class="row_heading level0 row3" >Hides, cattle, fresh</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col0" class="data row3 col0" >0.644473</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col1" class="data row3 col1" >0.549103</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col2" class="data row3 col2" >0.561979</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow3_col3" class="data row3 col3" >0.598171</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row4" class="row_heading level0 row4" >Meat indigenous, ass</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col0" class="data row4 col0" >0.618647</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col1" class="data row4 col1" >0.606011</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col2" class="data row4 col2" >0.612212</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow4_col3" class="data row4 col3" >0.664896</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row5" class="row_heading level0 row5" >Meat indigenous, bird nes</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col0" class="data row5 col0" >0.406118</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col1" class="data row5 col1" >0.47996</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col2" class="data row5 col2" >0.477989</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow5_col3" class="data row5 col3" >0.393133</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row6" class="row_heading level0 row6" >Meat indigenous, buffalo</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col0" class="data row6 col0" >0.524501</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col1" class="data row6 col1" >0.393947</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col2" class="data row6 col2" >0.319995</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow6_col3" class="data row6 col3" >0.466484</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row7" class="row_heading level0 row7" >Meat indigenous, camel</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col0" class="data row7 col0" >0.492636</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col1" class="data row7 col1" >0.475989</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col2" class="data row7 col2" >0.441158</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow7_col3" class="data row7 col3" >0.461859</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row8" class="row_heading level0 row8" >Meat indigenous, cattle</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col0" class="data row8 col0" >0.649031</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col1" class="data row8 col1" >0.562492</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col2" class="data row8 col2" >0.579772</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow8_col3" class="data row8 col3" >0.599394</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row9" class="row_heading level0 row9" >Meat indigenous, chicken</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col0" class="data row9 col0" >0.335482</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col1" class="data row9 col1" >0.506006</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col2" class="data row9 col2" >0.576824</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow9_col3" class="data row9 col3" >0.416985</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row10" class="row_heading level0 row10" >Meat indigenous, duck</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col0" class="data row10 col0" >0.285317</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col1" class="data row10 col1" >0.430394</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col2" class="data row10 col2" >0.4885</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow10_col3" class="data row10 col3" >0.369011</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row11" class="row_heading level0 row11" >Meat indigenous, geese</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col0" class="data row11 col0" >0.283109</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col1" class="data row11 col1" >0.29714</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col2" class="data row11 col2" >0.35201</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow11_col3" class="data row11 col3" >0.386369</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row12" class="row_heading level0 row12" >Meat indigenous, goat</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col0" class="data row12 col0" >0.419219</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col1" class="data row12 col1" >0.459889</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col2" class="data row12 col2" >0.46479</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow12_col3" class="data row12 col3" >0.496667</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row13" class="row_heading level0 row13" >Meat indigenous, horse</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col0" class="data row13 col0" >0.228973</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col1" class="data row13 col1" >0.178327</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col2" class="data row13 col2" >0.170462</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow13_col3" class="data row13 col3" >0.201469</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row14" class="row_heading level0 row14" >Meat indigenous, mule</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col0" class="data row14 col0" >0.384295</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col1" class="data row14 col1" >0.343165</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col2" class="data row14 col2" >0.350966</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow14_col3" class="data row14 col3" >0.492918</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row15" class="row_heading level0 row15" >Meat indigenous, other camelids</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col0" class="data row15 col0" >0.207807</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col1" class="data row15 col1" >0.13084</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col2" class="data row15 col2" >0.0869365</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow15_col3" class="data row15 col3" >0.25663</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row16" class="row_heading level0 row16" >Meat indigenous, pig</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col0" class="data row16 col0" >0.383557</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col1" class="data row16 col1" >0.596138</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col2" class="data row16 col2" >0.59727</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow16_col3" class="data row16 col3" >0.404523</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row17" class="row_heading level0 row17" >Meat indigenous, rabbit</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col0" class="data row17 col0" >0.452466</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col1" class="data row17 col1" >0.453528</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col2" class="data row17 col2" >0.46761</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow17_col3" class="data row17 col3" >0.429909</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row18" class="row_heading level0 row18" >Meat indigenous, rodents</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col0" class="data row18 col0" >-0.017406</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col1" class="data row18 col1" >-0.001253</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col2" class="data row18 col2" >0.0548468</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow18_col3" class="data row18 col3" >-0.033011</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row19" class="row_heading level0 row19" >Meat indigenous, sheep</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col0" class="data row19 col0" >0.449696</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col1" class="data row19 col1" >0.452507</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col2" class="data row19 col2" >0.453786</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow19_col3" class="data row19 col3" >0.505047</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row20" class="row_heading level0 row20" >Meat indigenous, turkey</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col0" class="data row20 col0" >0.0776512</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col1" class="data row20 col1" >0.141508</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col2" class="data row20 col2" >0.23715</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow20_col3" class="data row20 col3" >0.0815831</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row21" class="row_heading level0 row21" >Meat, ass</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col0" class="data row21 col0" >0.673004</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col1" class="data row21 col1" >0.667397</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col2" class="data row21 col2" >0.670024</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow21_col3" class="data row21 col3" >0.721188</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row22" class="row_heading level0 row22" >Meat, bird nes</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col0" class="data row22 col0" >0.398516</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col1" class="data row22 col1" >0.413742</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col2" class="data row22 col2" >0.407648</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow22_col3" class="data row22 col3" >0.390383</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row23" class="row_heading level0 row23" >Meat, buffalo</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col0" class="data row23 col0" >0.595647</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col1" class="data row23 col1" >0.42929</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col2" class="data row23 col2" >0.357446</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow23_col3" class="data row23 col3" >0.48325</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row24" class="row_heading level0 row24" >Meat, camel</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col0" class="data row24 col0" >0.577347</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col1" class="data row24 col1" >0.573849</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col2" class="data row24 col2" >0.527851</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow24_col3" class="data row24 col3" >0.561492</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row25" class="row_heading level0 row25" >Meat, cattle</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col0" class="data row25 col0" >0.611846</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col1" class="data row25 col1" >0.546762</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col2" class="data row25 col2" >0.565477</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow25_col3" class="data row25 col3" >0.588957</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row26" class="row_heading level0 row26" >Meat, chicken</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col0" class="data row26 col0" >0.322612</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col1" class="data row26 col1" >0.497971</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col2" class="data row26 col2" >0.565292</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow26_col3" class="data row26 col3" >0.407622</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row27" class="row_heading level0 row27" >Meat, duck</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col0" class="data row27 col0" >0.265477</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col1" class="data row27 col1" >0.38811</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col2" class="data row27 col2" >0.448873</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow27_col3" class="data row27 col3" >0.327401</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row28" class="row_heading level0 row28" >Meat, game</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col0" class="data row28 col0" >0.389236</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col1" class="data row28 col1" >0.482325</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col2" class="data row28 col2" >0.505708</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow28_col3" class="data row28 col3" >0.404113</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row29" class="row_heading level0 row29" >Meat, goat</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col0" class="data row29 col0" >0.37308</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col1" class="data row29 col1" >0.3989</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col2" class="data row29 col2" >0.405535</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow29_col3" class="data row29 col3" >0.442325</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row30" class="row_heading level0 row30" >Meat, goose and guinea fowl</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col0" class="data row30 col0" >0.310403</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col1" class="data row30 col1" >0.337075</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col2" class="data row30 col2" >0.393374</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow30_col3" class="data row30 col3" >0.400975</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row31" class="row_heading level0 row31" >Meat, horse</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col0" class="data row31 col0" >0.240358</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col1" class="data row31 col1" >0.161244</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col2" class="data row31 col2" >0.154695</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow31_col3" class="data row31 col3" >0.253028</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row32" class="row_heading level0 row32" >Meat, mule</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col0" class="data row32 col0" >0.371703</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col1" class="data row32 col1" >0.330178</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col2" class="data row32 col2" >0.331309</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow32_col3" class="data row32 col3" >0.482602</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row33" class="row_heading level0 row33" >Meat, nes</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col0" class="data row33 col0" >0.263154</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col1" class="data row33 col1" >0.298796</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col2" class="data row33 col2" >0.340809</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow33_col3" class="data row33 col3" >0.288018</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row34" class="row_heading level0 row34" >Meat, other camelids</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col0" class="data row34 col0" >0.433639</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col1" class="data row34 col1" >0.384046</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col2" class="data row34 col2" >0.373344</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow34_col3" class="data row34 col3" >0.47001</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row35" class="row_heading level0 row35" >Meat, other rodents</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col0" class="data row35 col0" >-0.00404508</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col1" class="data row35 col1" >0.00799845</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col2" class="data row35 col2" >0.0557307</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow35_col3" class="data row35 col3" >-0.0229908</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row36" class="row_heading level0 row36" >Meat, pig</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col0" class="data row36 col0" >0.368533</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col1" class="data row36 col1" >0.588932</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col2" class="data row36 col2" >0.583096</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow36_col3" class="data row36 col3" >0.387766</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row37" class="row_heading level0 row37" >Meat, rabbit</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col0" class="data row37 col0" >0.399239</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col1" class="data row37 col1" >0.397631</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col2" class="data row37 col2" >0.416648</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow37_col3" class="data row37 col3" >0.3688</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row38" class="row_heading level0 row38" >Meat, sheep</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col0" class="data row38 col0" >0.459739</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col1" class="data row38 col1" >0.447937</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col2" class="data row38 col2" >0.445679</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow38_col3" class="data row38 col3" >0.501001</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row39" class="row_heading level0 row39" >Meat, turkey</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col0" class="data row39 col0" >0.0446689</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col1" class="data row39 col1" >0.141992</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col2" class="data row39 col2" >0.232042</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow39_col3" class="data row39 col3" >0.061515</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row40" class="row_heading level0 row40" >Milk, whole fresh buffalo</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col0" class="data row40 col0" >0.377427</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col1" class="data row40 col1" >0.395695</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col2" class="data row40 col2" >0.355487</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow40_col3" class="data row40 col3" >0.422006</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row41" class="row_heading level0 row41" >Milk, whole fresh camel</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col0" class="data row41 col0" >0.582061</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col1" class="data row41 col1" >0.560904</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col2" class="data row41 col2" >0.53383</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow41_col3" class="data row41 col3" >0.572511</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row42" class="row_heading level0 row42" >Milk, whole fresh cow</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col0" class="data row42 col0" >0.575445</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col1" class="data row42 col1" >0.590129</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col2" class="data row42 col2" >0.641824</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow42_col3" class="data row42 col3" >0.564405</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row43" class="row_heading level0 row43" >Milk, whole fresh goat</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col0" class="data row43 col0" >0.42863</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col1" class="data row43 col1" >0.432774</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col2" class="data row43 col2" >0.420051</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow43_col3" class="data row43 col3" >0.468469</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row44" class="row_heading level0 row44" >Milk, whole fresh sheep</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col0" class="data row44 col0" >0.484644</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col1" class="data row44 col1" >0.466679</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col2" class="data row44 col2" >0.471685</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow44_col3" class="data row44 col3" >0.553379</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row45" class="row_heading level0 row45" >Skins, goat, fresh</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col0" class="data row45 col0" >0.403191</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col1" class="data row45 col1" >0.441643</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col2" class="data row45 col2" >0.439507</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow45_col3" class="data row45 col3" >0.465534</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row46" class="row_heading level0 row46" >Skins, sheep, fresh</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col0" class="data row46 col0" >0.46452</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col1" class="data row46 col1" >0.448705</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col2" class="data row46 col2" >0.44143</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow46_col3" class="data row46 col3" >0.5217</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row47" class="row_heading level0 row47" >Skins, sheep, with wool</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col0" class="data row47 col0" >0.382813</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col1" class="data row47 col1" >0.375227</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col2" class="data row47 col2" >0.380435</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow47_col3" class="data row47 col3" >0.467755</td>
            </tr>
            <tr>
                        <th id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3elevel0_row48" class="row_heading level0 row48" >Snails, not sea</th>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col0" class="data row48 col0" >0.518544</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col1" class="data row48 col1" >0.312585</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col2" class="data row48 col2" >-0.291296</td>
                        <td id="T_96b37bf2_2306_11ea_8a32_cda3d6ffcd3erow48_col3" class="data row48 col3" >0.435402</td>
            </tr>
    </tbody></table>



### 3.3. Which produce generates the most emission per unit ?
---
Studying the overall impact of each produce is interesting, but these values can be biased by the fact that there are more animals. It would be interesting to see what is the impact of each product, per unit.

Most emissions here are computed for each animal, and we included Rice too, where emissions are expressed in Gigagrams/hectar/year, while animals are in Gigagrams/Head / year.



![png](assets/img/output_88_0.png)


This plot is very intersting, as it confirms previous findings: Cattle seem to be a a huge contributor to emissions, with an emission factor of 0.002 Gigagrams / Head or 2 metric tonnes per year. Compared to poultry animals this is huge. This suggests that reducing the population of cattle and increasing the population of Chickens, would in fact have a positive impact on reducing the global emissions. 

This would also mean reducing the amount of produce generated from cattle: Milk, Beef and skins.
