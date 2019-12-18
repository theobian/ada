---
layout: post
title:  "Exploration"
description: Interpretating results.
---

# Environmental Impact of Agricultural Practices in the World


---
## 1. What is the overall impact of the agriculture industry on global green house gas (GHG) emissions ?
---

This first question that naturally comes to mind. FAO provides data regarding emissions from multiple sectors. Green house gase emissions are computed using `CO2eq` (i.e. CO2 equivalent) from multiple gases (CO2, CH4, N20, and F-gases), which are in top list of Green House Gases.


```python
emissions_by_sector_df = pd.read_csv("../data_cleaned/environment/Environment_Emissions_by_Sector_E_All_Data_(Normalized).csv")
emissions_by_sector_df = emissions_by_sector_df[emissions_by_sector_df.areacode.isin(country_groups['countrygroupcode'].unique())]
sns.set_palette(sns.color_palette("Paired", 11))

plot_stacked_bar_single_area_single_element(emissions_by_sector_df, elementcode=7263, areacode=5000, title="Worldwide shares of emissions by sector", ylabel="% of global emissions")
```


![png](assets/img/output_9_0.png)


It seems that agriculture has stayed around 10% of global emissions by sector for the years 1990-2010. Now we shall look at the share of this emissions for each gas, only looking at the World wide Agriculture emissions.


```python
plot_elements_pie_single_area(emissions_by_sector_df, elementcodes=[7264, 7265, 7266], areacode=5000, suptitle="Average shares of GHG emissions by sector (1990-2000 period)")
```


![png](assets/img/output_11_0.png)


From this pie chart, we can learn a few things for the Agriculture industry:
 - It seems that direct CO2 emissions from Agriculture are absent (0%). This makes sense as CO2 is not directly emitted. However, the CO2 emissions might be indirect, as food is always transported via non carbon-free methods, and industrial machinery is used in agriculture, and requires energy.
 - Global CH4 Emissions are shared between Agriculture and Energy industries, with a majority for Agriculture (41.4%)
 - Global N2O are largely dominated by the Agriculture industry (70%)

All of these gases are considered top level Green House gases. It makes sense now to focus on searching where those emissions come from in detail (only for agriculture), and how can we reduce them without comprimising the diet of the population.

Now we know which GHG are largely emitted by the agriculture industry, and that Agriculture contributes to roughly 10% of global Emissions, but largely dominates other sectors in terms of CH4 and N2O emissions. 

However, this plot does not take into consideration indirect emissions due to Agriculture:
- Emissions due to transport of food (included in "Transport" sector)
- Emissions due to use of energy for producing agricultural products (included in "Energy")

Our analysis focuses more on the direct emissions of Agriculture, and hence we will not take those aspects in consideration as they fall outside of the scope.

---
### 1.1. What are the sources of CH4 and N2O emissions from in the Agriculture Industry ?
---

To illustrate this, we can separate the emissions of both gases into 10 items related to agriculture: Enteric Fermentation, Manure management, Rice Cultivation, Synthetic Fertilizers, Manure applied to soils, Manure left on Pasture, Crop residues, Burning of crop residues, Burning of savanna and Cultivation of organic Soils.



```python
emissions_agr_df = pd.read_csv("../data_cleaned/emissions_agriculture/Emissions_Agriculture_Agriculture_total_E_All_Data_(Normalized).csv")
emissions_agr_df_grp = groupby_country_groups(emissions_agr_df, country_groups)
emissions_agr_df_grp = emissions_agr_df_grp[emissions_agr_df_grp.year < 2020]

```


```python
plot_elements_pie_single_area(emissions_agr_df_grp, [7225, 7230], 5000, "Average yearly shares of CH4 and N2O emissions for agriculture (1961-2017 period)", figsize=(15, 10), y_title=0.9)
```


![png](assets/img/output_15_0.png)


This pie chart illustrates quite well the origin of emissions of CH4 and N2O, in the agriculture industry. Before interpreting the chart, let's brievly explain what each item represents:
- Burning - Crop residues: Agricultural practice that consists of combusting a percentage of crop residues on site
- Burning - Savanna: Periodic prescribed burning of savanna for agricultural purposes
- Enteric Fermentation: Digestive process by which carbohydrates are broken down by micro organisms into simple molecules for absorption into the bloodstream of an animal.
- Manure Management: Refers to capture, storage, treatment, and utilization of animal manure
- Rice Cultivation: Agricultural practice for growing rice seeds
- Crop Resdiues: Agriculture management practice that consists in returning to managed soils the residual part of the produce
- Cultivation of Organic Soils:
- Manure applied to Soils: Animal waste distributed on fields in amounts that enrich soils
- Manure left on pasture: Animal waste left on managed soils from grazing livestock. 
- Synthetic Fertilizers: Inorganic material of synthetic origin added to a soil to supply one or more plant nutrients essential to the growth of plants.

1. CH4 Emissions:

    - Direct CH4 emissions of agriculture are mostly dominated by the Enteric Fermentation of Livestock (69.4%), which means that this particular source of emissions accounts for rougly 30% of the global CH4 Emissions, which is quite significant.
    - Rice Cultivation also is a big contributor (18%) to the emissions of this GHG.
    - Other sources have much lower contribution to emissions of this gas
    

2. N2O Emissions:
    - The biggest contributor is "Manure Left on Pasture", followed by Synthetic Fertilizers.
    - The use of Manure (Manure management, left on pasture, and applied to soils) have a contribution of roughly 40% (together) of N2O Emissions for agriculture.

---
### 1.2. How have global emissions of those gases from each source evolved in the past years ?
---
Having an average share of each source over the past 50 years gives us a general idea of where the emissions come from. Additionally, the evolution of emissions in this time frame is also interesting.

We all know Global emissions have increased worldwide, but what are the sources of this increase in the agricultural sector ?


```python
plot_stacked_bar_single_area_single_element(emissions_agr_df_grp, elementcode=7225, areacode=5000, title="Worldwide evolution of CH4 Emissions by source", ylabel="Gigagrams", bbox=(1.4, 0.5), width=0.5)
```


![png](assets/img/output_19_0.png)



```python
plot_stacked_bar_single_area_single_element(emissions_agr_df_grp, elementcode=7230, areacode=5000, title="Worldwide evolution of N2O Emissions by source", ylabel="Gigagrams", bbox=(1.5, 0.5), width=0.5)
```


![png](assets/img/output_20_0.png)


We can notice a clear linear increase in the emission of both gases , with a slight peak in 1990-1995. We can see that some items only start appearing around that period of time, so this explains the spike.

#### 1. Emissions of CH4:

As seen previously, we knew that CH4 emissions are dominated by the Enteric Fermentation, and we can see that it has increased by roughly 50% since 1961. However other sources do not seem to have had the same increase in emissions.

#### 2. Emissions of N2O:
Increases here are more interesting. We can see that emissions due to Synthetic fertilizers have increased linearly by almost 400%, with slightly lower steepness after ~1995. The reason for this seems to be the same as for CH4 Emissions: additional information haas been added
Manure Management's emissions also increased linearly.

---
### 1.3. Which countries contribute the most to emissions due to agriculture ?
---

We now have a global view on emissions worldwide, but it would be interesting to have a more detailed approach and see which countries countribute the most to the emissions of those 2 gases.

#### 1. Raw data
First we plot the total emissions in gigagrams for each country and gas (for CH4 and N2O) as a heatmap.


```python
emissions_by_sector_df[emissions_by_sector_df.itemcode == 1711]
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
      <th>areacode</th>
      <th>area</th>
      <th>itemcode</th>
      <th>item</th>
      <th>elementcode</th>
      <th>element</th>
      <th>year</th>
      <th>unit</th>
      <th>value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>464088</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1990</td>
      <td>Gigagrams</td>
      <td>4.572738e+06</td>
    </tr>
    <tr>
      <th>464089</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1991</td>
      <td>Gigagrams</td>
      <td>4.551383e+06</td>
    </tr>
    <tr>
      <th>464090</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1992</td>
      <td>Gigagrams</td>
      <td>4.529691e+06</td>
    </tr>
    <tr>
      <th>464091</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1993</td>
      <td>Gigagrams</td>
      <td>4.497534e+06</td>
    </tr>
    <tr>
      <th>464092</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1994</td>
      <td>Gigagrams</td>
      <td>4.528782e+06</td>
    </tr>
    <tr>
      <th>464093</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1995</td>
      <td>Gigagrams</td>
      <td>4.574938e+06</td>
    </tr>
    <tr>
      <th>464094</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1996</td>
      <td>Gigagrams</td>
      <td>4.589671e+06</td>
    </tr>
    <tr>
      <th>464095</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1997</td>
      <td>Gigagrams</td>
      <td>4.573246e+06</td>
    </tr>
    <tr>
      <th>464096</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1998</td>
      <td>Gigagrams</td>
      <td>4.607203e+06</td>
    </tr>
    <tr>
      <th>464097</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>1999</td>
      <td>Gigagrams</td>
      <td>4.654865e+06</td>
    </tr>
    <tr>
      <th>464098</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2000</td>
      <td>Gigagrams</td>
      <td>4.641466e+06</td>
    </tr>
    <tr>
      <th>464099</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2001</td>
      <td>Gigagrams</td>
      <td>4.667997e+06</td>
    </tr>
    <tr>
      <th>464100</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2002</td>
      <td>Gigagrams</td>
      <td>4.674281e+06</td>
    </tr>
    <tr>
      <th>464101</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2003</td>
      <td>Gigagrams</td>
      <td>4.702336e+06</td>
    </tr>
    <tr>
      <th>464102</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2004</td>
      <td>Gigagrams</td>
      <td>4.803971e+06</td>
    </tr>
    <tr>
      <th>464103</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2005</td>
      <td>Gigagrams</td>
      <td>4.853465e+06</td>
    </tr>
    <tr>
      <th>464104</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2006</td>
      <td>Gigagrams</td>
      <td>4.906533e+06</td>
    </tr>
    <tr>
      <th>464105</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2007</td>
      <td>Gigagrams</td>
      <td>4.994814e+06</td>
    </tr>
    <tr>
      <th>464106</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2008</td>
      <td>Gigagrams</td>
      <td>5.013850e+06</td>
    </tr>
    <tr>
      <th>464107</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2009</td>
      <td>Gigagrams</td>
      <td>5.025268e+06</td>
    </tr>
    <tr>
      <th>464108</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7231</td>
      <td>Emissions (CO2eq)</td>
      <td>2010</td>
      <td>Gigagrams</td>
      <td>5.077485e+06</td>
    </tr>
    <tr>
      <th>464109</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1990</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464110</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1991</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464111</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1992</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464112</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1993</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464113</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1994</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464114</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1995</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464115</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1996</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464116</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1997</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>464117</th>
      <td>5000</td>
      <td>World</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7194</td>
      <td>Emissions (CO2eq) from CO2</td>
      <td>1998</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>546685</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2002</td>
      <td>%</td>
      <td>4.919950e+01</td>
    </tr>
    <tr>
      <th>546686</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2003</td>
      <td>%</td>
      <td>4.946090e+01</td>
    </tr>
    <tr>
      <th>546687</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2004</td>
      <td>%</td>
      <td>4.975780e+01</td>
    </tr>
    <tr>
      <th>546688</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2005</td>
      <td>%</td>
      <td>4.932800e+01</td>
    </tr>
    <tr>
      <th>546689</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2006</td>
      <td>%</td>
      <td>4.940030e+01</td>
    </tr>
    <tr>
      <th>546690</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2007</td>
      <td>%</td>
      <td>4.990520e+01</td>
    </tr>
    <tr>
      <th>546691</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2008</td>
      <td>%</td>
      <td>4.931350e+01</td>
    </tr>
    <tr>
      <th>546692</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2009</td>
      <td>%</td>
      <td>4.920320e+01</td>
    </tr>
    <tr>
      <th>546693</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7269</td>
      <td>Share of N2O in sector emissions</td>
      <td>2010</td>
      <td>%</td>
      <td>4.937940e+01</td>
    </tr>
    <tr>
      <th>546694</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1990</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546695</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1991</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546696</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1992</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546697</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1993</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546698</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1994</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546699</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1995</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546700</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1996</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546701</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1997</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546702</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1998</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546703</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>1999</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546704</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2000</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546705</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2001</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546706</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2002</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546707</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2003</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546708</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2004</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546709</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2005</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546710</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2006</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546711</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2007</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546712</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2008</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546713</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2009</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>546714</th>
      <td>5873</td>
      <td>OECD</td>
      <td>1711</td>
      <td>Agriculture total</td>
      <td>7180</td>
      <td>Share of F-gases in sector emissions</td>
      <td>2010</td>
      <td>Gigagrams</td>
      <td>0.000000e+00</td>
    </tr>
  </tbody>
</table>
<p>10808 rows × 9 columns</p>
</div>




```python
SHAPE_FILE = "../data/gpd_maps/ne_110m_admin_0_countries.shp"
titles = {7225: "Emissions of CH4 by country in 2017", 7230: "Emissions of N2O by country in 2017", 7231: "Emissions in CO2eq by country in 2017"}
#plot_maps(emissions_agr_df, [7225, 7230, 7231], country_codes, 2017, SHAPE_FILE, titles=titles)
plot_maps(emissions_agr_df, [7231], country_codes, 2017, SHAPE_FILE, titles=titles, unit="Gigagrams")
```

    <matplotlib.colors.Normalize object at 0x000002430C604CC0>
    


![png](assets/img/output_25_1.png)


It looks like 4-5 countries contribute much more than others to emissions of the two gases: China, India, United States, Brazil and Australia. However, these countries' populations are quite signifcant. Let's look at the same graph, but after normalizing by population.

#### 2. Normalized by population



```python
titles = {7225: "Emissions per capita of CH4 by country in 2017", 7230: "Emissions per capita of N2O by country in 2017", 7231: "Emissions per capita of CO2eq by country in 2017"}

# This function first groups all items per country/year (for each element) and normalize by population of each year
emissions_agr_df_norm = normalize_by_population(groupby_all_items_sum(emissions_agr_df), population_df)
#plot_maps(emissions_agr_df_norm, [7225, 7230, 7231], country_codes, 2017, SHAPE_FILE, titles=titles)
plot_maps(emissions_agr_df_norm, [7231], country_codes, 2017, SHAPE_FILE, titles=titles, unit="Gigagrams")
```

    <matplotlib.colors.Normalize object at 0x000002430C3C8B70>
    


![png](assets/img/output_28_1.png)


At a first glance, it seems that all countries have similar values of emission gigagrams/capita, but the scale tells us that some countries have higher values. Let's plot the distribution of values and check how it behaves.


```python
fig, ax = plt.subplots(figsize=(15, 5), ncols=2)
tmp1 = emissions_agr_df_norm[emissions_agr_df_norm.elementcode == 7225]
tmp2 = emissions_agr_df_norm[emissions_agr_df_norm.elementcode == 7230]
sns.distplot(tmp1['value'].dropna(), ax=ax[0])
ax[0].set_title("Distribution of CH4 emissions gigagrams/capita")
sns.distplot(tmp2['value'].dropna(), ax=ax[1])
ax[1].set_title("Distribution of N2O emissions gigagrams/capita");

```

    C:\Users\theop\Anaconda3\lib\site-packages\scipy\stats\stats.py:1713: FutureWarning:
    
    Using a non-tuple sequence for multidimensional indexing is deprecated; use `arr[tuple(seq)]` instead of `arr[seq]`. In the future this will be interpreted as an array index, `arr[np.array(seq)]`, which will result either in an error or a different result.
    
    


![png](assets/img/output_30_1.png)


The values seem to be very concentrated around 0, but both distributions have a very long tail. This could be due to a faulty value for one or a couple of countries.

After further inspection, we saw that one country seems to stand out and has a much higher value: Falkland Islands, a small group of islands in the southern Atlantic, with a population of around 3000 people. These islands seem to have a quite high livestock/capita ratio, according to their website [Falkland Government Website](https://www.fig.gov.fk/agriculture/publications/farming-stastics/category/27-farming-statistics-2016-to-2020). For visualization purposes, we will drop this line and replot the maps.


```python
plot_maps(emissions_agr_df_norm[emissions_agr_df_norm.areacode != 65], [7231], country_codes, 2017, SHAPE_FILE, titles=titles, unit="Gigagrams/capita")
```

    <matplotlib.colors.Normalize object at 0x000002430C378320>
    


![png](assets/img/output_32_1.png)


The map looks much better now. We can see which countries stand out: Australia and Mongolia seem to have a very high emission factor per capita for both gases.

### 1.4. Which countries contribute the most to emissions due to agriculture ?
---
Before pursuing further, it would also be useful to have an evolution of emissions of different countries over time. Such a visualization requires us to use interactive maps with a slider to change the years



```python
from fao_ada.plotting import plot_world_map_slider
```


```python
#plot_world_map_slider(emissions_agr_df[(emissions_agr_df.elementcode == 7231)], "test", "test", "Gigagrams")
```

---
## 2. How has the agriculture industry evolved in the time frame ?
---
Now that we have a general idea on the different gas emissions due to agriculture, as well as information on which countries contribute to emissions, we will look through a different lens, and study the evolution of the industry over the given time frame

### 2.1. What kind of crops/livestock increased in production in this time frame ?
---
We will now shift our focus to production of various crops and livestock. The data is separated in 3 categories: Livestock (live animals), Livestock produce (meat, eggs, etc..) and Crops.

#### 1. Evolution of Livestock stocks


```python
from fao_ada.pre_processing.grouping import groupby_item_groups
livestock_df = pd.read_csv("../data_cleaned/production/Production_Livestock_E_All_Data_(Normalized).csv")
livestock_df_grpd = groupby_country_groups(livestock_df, country_groups)

```


```python
sns.set_palette(sns.color_palette("Paired", 11))
plot_stacked_bar_single_area_single_element(livestock_df_grpd, elementcode=5111, areacode=5000, title="Evolution of Livestock stocks (Heads)", ylabel="Heads", bbox=(1.3, 0.5), width=0.5)
sns.set_palette(sns.color_palette("Paired", 7))
plot_stacked_bar_single_area_single_element(livestock_df_grpd, elementcode=5112, areacode=5000, title="Evolution of Livestock stocks (1000 Heads)", ylabel="1000 Heads", bbox=(1.4, 0.5), width=0.5)
```


![png](assets/img/output_41_0.png)



![png](assets/img/output_41_1.png)


As expected, of course, all stocks of live animals have increased. These take into consideration all animals used to produce food: it can be dairy cattle, layer chicken etc.. 

Now we normalize by population to see if the increase is proportional to the increase in population


```python
livestock_df_grpd_norm = normalize_by_population(livestock_df_grpd, population_df)
sns.set_palette(sns.color_palette("Paired", 11))
plot_stacked_bar_single_area_single_element(livestock_df_grpd_norm, elementcode=5111, areacode=5000, title="Evolution of Livestock stocks (Heads/capita)", ylabel="Heads/capita", bbox=(1.3, 0.5), width=0.5)
sns.set_palette(sns.color_palette("Paired", 7))
plot_stacked_bar_single_area_single_element(livestock_df_grpd_norm, elementcode=5112, areacode=5000,factor=1000, title="Evolution of Livestock stocks (Heads/capita)", ylabel="Heads/capita", bbox=(1.4, 0.5), width=0.5)
```


![png](assets/img/output_43_0.png)



![png](assets/img/output_43_1.png)


Surprisingly, the amount of "Sheep and Goats" and "Cattle and Buffaloes" per capita seems to be decreasing, while for Poultry birds it is clearly increasing. 
This could be due to multiple factors:
- Cattle, Sheep and Goats need more time to grow, enducing a higher cost in production
- Poultry Birds are cheaper to feed, need less space to grow, and we have developped techniques where they can be stacked by millions easily, which is not the case for bigger animals.
- The increase in population was more dominant in countries where Red meat consumption is lower (India).
- People prefer to eat chicken today rather than in the 60s

In 2017, there was 3 chickens per living person on earth.

#### 2. Evolution of production of Livestock products


```python
livestock_prim_df = pd.read_csv("../data_cleaned/production/Production_LivestockPrimary_E_All_Data_(Normalized).csv")
livestock_prim_itemgroups = load_dataframe("../data/item_groups/Production_Livestock_Primary_All_data.csv")
get_itemgroups_intersections(livestock_prim_itemgroups)

print("\n Elements in DF: \n")
print_all_elements(livestock_prim_df)
```

    Intersection on Meat, Total (1765) and Meat indigenous, total (1770) on {(1176, 'Snails, not sea'), (1163, 'Meat, game'), (1166, 'Meat nes')}
    Intersection on Meat, Total (1765) and Beef and Buffalo Meat (1806) on {(947, 'Meat, buffalo'), (867, 'Meat, cattle')}
    Intersection on Meat, Total (1765) and Sheep and Goat Meat (1807) on {(977, 'Meat, sheep'), (1017, 'Meat, goat')}
    Intersection on Meat, Total (1765) and Meat, Poultry (1808) on {(1069, 'Meat, duck'), (1080, 'Meat, turkey'), (1073, 'Meat, goose and guinea fowl'), (1058, 'Meat, chicken'), (1089, 'Meat, bird nes')}
    Intersection on Meat indigenous, total (1770) and Meat indigenous, poultry (1775) on {(1070, 'Meat indigenous, duck'), (1087, 'Meat indigenous, turkey'), (1084, 'Meat indigenous, bird nes'), (1077, 'Meat indigenous, geese'), (1094, 'Meat indigenous, chicken')}
    
     Elements in DF: 
    
          elementcode                        element       unit
    0            5313                         Laying  1000 Head
    57           5410                          Yield   100mg/An
    114          5510                     Production     tonnes
    171          5320  Producing Animals/Slaughtered       Head
    224          5420                          Yield      hg/An
    330          5322                     Production       Head
    383          5417           Yield/Carcass Weight      hg/An
    648          5323                     Production  1000 Head
    701          5424           Yield/Carcass Weight    0.1g/An
    1467         5321  Producing Animals/Slaughtered  1000 Head
    2037         5318                   Milk Animals       Head
    

We can ommit the itemgroup `Meat, total` as it comprises of all other item groups related to meat, and drop the elements that are not summable (related to yield).
Also, we need to be careful as `Meat indigenous, total` intersects with `Meat indigenous, poultry`


```python
livestock_prim_df_grpd = groupby_item_groups(livestock_prim_df, livestock_prim_itemgroups, drop_elements=[5410, 5420, 5417, 5424], 
                                             except_={1765: ("Meat, Other", 10001), 1770: ("Meat indigenous, other", 10002)})
livestock_prim_df_grpd = groupby_country_groups(livestock_prim_df_grpd, country_groups)
sns.set_palette(sns.color_palette("Paired", 9))
plot_stacked_bar_single_area_single_element(livestock_prim_df_grpd, elementcode=5510, areacode=5000, title="Evolution of Livestock produce production", ylabel="Tonnes", bbox=(1.4, 0.5), width=0.5)
```


![png](assets/img/output_48_0.png)


There seems to be a drop in production of `Meat indigenous, poultry` and `Meat indegenous, other`, and after inspection, it seems this data is missing for the years 2014 up to 2017. If we need to, we can use time series to complete the items related to this itemgroup for each country. 

Also, we can notice clear drastic increases in all productions, but we need to factor in the growth in population too. For that, we normalize by the world population as done earlier


```python
livestock_prim_df_grpd_norm = normalize_by_population(livestock_prim_df_grpd, population_df)
plot_stacked_bar_single_area_single_element(livestock_prim_df_grpd_norm, elementcode=5510, areacode=5000, title="Evolution of Livestock produce production (tonnes/capita)", ylabel="Tonnes/capita", bbox=(1.4, 0.5), width=0.5)
```


![png](assets/img/output_50_0.png)


What this graph tells us:
- The overall production of livestock produce did not increase a lot (per capita) during 1961-1995, but took quite a signifcant upward trend in the last 2 decades (1995-2015), growing from 175kg per capita to 200kg per capita (14% increase in 20 years).
- Beef/buffalo meat did not increase a lot in terms of tonnes/capita, as well as Milk production.
- The most flagrant increases in tonnes/capita are in `poultry` meat (`indegenous` and regular), as well as `Indegenous meat`, but it contains the latter.

# MAYBE ADD MAP OF COUNTRIES' TOP PRODUCTION

#### 3. Evolution of Crops production


```python
crops_df = pd.read_csv("../data_cleaned/production/Production_Crops_E_All_Data_(Normalized).csv")
crops_itemgroups = load_dataframe("../data/item_groups/Production_Crops_All_data.csv")
print(f"The elements are: \n")
print_all_elements(crops_df)
```

    The elements are: 
    
        elementcode         element    unit
    0          5312  Area harvested      ha
    43         5419           Yield   hg/ha
    85         5510      Production  tonnes
    

The `itemgroups` here are quite overlapping, and it is hard to actually decide which to drop and which not. For visualization purposes, we will keep all item groups, but the some itemgroups intersect and are not exclusive. 

The itemgroup `All crops` has been dropped, as it overlaps with a lot of other groups. However, we kept all items that are only present in this itemgroup and named the new itemgroup `Other crops`


```python
crops_df_grpd = groupby_item_groups(crops_df, crops_itemgroups, drop_elements=[5419], except_={1714: ("Other Crops", 10002)})
crops_df_grpd = groupby_country_groups(crops_df_grpd, country_groups)
```


```python
sns.set_palette(sns.color_palette(palette))
plot_stacked_bar_single_area_single_element(crops_df_grpd, elementcode=5510, areacode=5000, title="Evolution of Crops Production (tonnes)", ylabel="Tonnes", width=0.5)
```


![png](assets/img/output_57_0.png)



```python
crops_df_grpd_norm = normalize_by_population(crops_df_grpd, population_df)
plot_stacked_bar_single_area_single_element(crops_df_grpd_norm, elementcode=5510, areacode=5000, title="Evolution of Crops Production (Tonnes/Capita)", ylabel="Tonnes/capita", width=0.5)
```


![png](assets/img/output_58_0.png)



```python
line_plot_single_element_single_area(crops_df_grpd_norm, elementcode=5510, areacode=5000, title="Evolution of Crops Production (Tonnes/Capita)", ylabel="Tonnes/capita")
```


![png](assets/img/output_59_0.png)


The overall shape of the bars are similar to livestock production: 
- We can see an increase in tonnes/capita between the 60s and 70s, and a stagnation after that. And another significant increase in the years after 2000.
- Production per capita seems to have had an increase in: `cereals`, `vegetables`, `fruits`, and `other crops`

### 2.2. How did Synthetic Fertilizer use change over time ? And what is was it's effect on production/yield and GHG emissions ?
---

This question is more related to crops. This type of Fertilizers started being used in the beginnin of the 20th century, after Fritz Haber inventing Haber–Bosch process, a method used in industry to synthesize ammonia from nitrogen gas and hydrogen gas.[[1]](https://en.wikipedia.org/wiki/Fritz_Haber)

Greenhouse gas (GHG) emissions from synthetic fertilizers consist of nitrous oxide gas from synthetic nitrogen additions to managed soils. Specifically, N2O is produced by microbial processes of nitrification and de-nitrification taking place on the addition site (direct emissions), and after volatilization/re-deposition and leaching processes (indirect emissions)


```python
fertilizer_df = pd.read_csv("../data_cleaned/emissions_agriculture/Emissions_Agriculture_Synthetic_Fertilizers_E_All_Data_(Normalized).csv")
fertilizer_df = fertilizer_df[fertilizer_df.year < 2020]
fertilizer_df['item'] = fertilizer_df['item'].apply(lambda x: x if x != "Nitrogenous fertilizers" else "Nutrient nitrogen N (total)")
fertilizer_df['itemcode'] = fertilizer_df['itemcode'].apply(lambda x: x if x != 1360 else 3102)

fertilizer_df['element'] = fertilizer_df['element'].apply(lambda x: x if x != "Agricultural Use in nutrients" else "Agricultural Use")
fertilizer_df['unit'] = fertilizer_df['unit'].apply(lambda x: x if x != "kg of nutrients" else "kg")
fertilizer_df['elementcode'] = fertilizer_df['elementcode'].apply(lambda x: x if x != 5162 else 5163)
fertilizer_df_grpd = groupby_country_groups(fertilizer_df, country_groups, drop_elements=[72293])
```

#### 1. History of Fertilizer use

We are only provided with the use of Nitrogenous fertilizers, and its related emissions.


```python
line_plot_single_element_single_area(fertilizer_df_grpd, elementcode=5163, areacode=5000, title="Agricultural use of Synthetic fertilizers (kg)", ylabel="kg")
```


![png](assets/img/output_64_0.png)


Along this time frame (1961-2017) the use of synthetic fertilizers been multiplied by at least 5, which is pretty impressive.

It would be interesting to see if the the increase in yield is similar (by factoring out the increase in production of course). For that, we would need to study the amount of fertilizers used per ton of production, and relate this quantity to the yield of each product. However, this dataset is quite limited, as we only know the overall use of fertilizers, and not for each crop, making it quite hard to study this. 

Despite that, our analysis is more focused on the environmental impact of the industry, so we will concentrate on the emissions due to the use of those fertilizers.

#### 2. Emissions due to synthetic fertilizers

As previously mentionned, synthetic fertilizers generate N2O in either a direct way, or an indirect way. However, to be fair with our comparisons later on, we will express those values in terms of COeq (i.e. the equivalent of N2O in CO2, because N2O has much higher GHG effects than CO2)



```python
from fao_ada.plotting import plot_stacked_bar_single_area_single_item
sns.set_palette(sns.color_palette("husl", 2))
plot_stacked_bar_single_area_single_item(fertilizer_df_grpd, 3107, [72353, 72373], areacode=5000, title="Emissions due to the use of synthetic fertilizers (CO2eq)", ylabel="Gigagrams", width=0.5)
```


![png](assets/img/output_67_0.png)




 
