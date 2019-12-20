---
layout: post
title:  "4: Nutrition"
description: Investigating nutritional values.
---


## Constructing a diet based on nutrient needs


### Diet diversity
Nutrients are contained in different quantities in different commodities; for example:
- roots and tubers contain a lot of vitamin A but a low amount of protein
- livestock and fish contain a lot of protein and vitamin B12
- some nutrients are generally harder to come by than others
A healthy diet requires food intake diversity.

### Malnutrition
The first cause of death by malnutrition is caused by a lack of protein. The most common mineral deficiency is iron deficiency.

Different regions have different diets and different deficiencies. In the USA for example, the nutrients that are under-consumed are fiber, calcium, vitamin D and potassium. However, in less-developped countries, there are a lot of iron and protein deficiencies.


### Meat vs. plants:
Plants are a fairly poor substitute for some of the nutrients meat provides. For example, iron and zinc contents in plants are very low. The main nutrients plants lack in high quantities are Vitamin A, Thiamin, Vitamin B12, zince and Calcium.

A diet relying more on plants rather than solely on meat is in accordance with most health councils and organizations. 
Vitamin B12 is mainly found in meat. Vitamin A is mainly found in butter, liver, and in carotenoids to some extent. Thiamin is found in meat and dairy, and cereals to a lesser extent. Calcium is mainly found in milk dairy, and cereals and vegetables to a much lesser extent. 


## Creating a nutrient list
These nutrients are deemed to be essential not only because of their paramount importance to a healthy diet but also because of the fact that there exists widespread deficiencies worldwide.

Some of these can be easily manufactured and distributed (e.g. iodine). We will only focus on a subset of nutrients, and look at protein content, fiber content, lipid content, vitamin content and mineral content of given foods in order to construct a "healthy" diet (meaning one that provides good nutrient intake).

- Proteins
- Carbohydrates
- Fibers
- Lipids
- Vitamins and minerals
    - Vitamins: A, B6, B9, B12, C, D, E
    - Minerals : Fe, Ca
    

# Nutrient value database
In parallel with the evaluation of the environmental impact of livestock and crops, we need to decide which food yield the best (or at least a good/healthy enough) nutritive value. 
To do this, after having decided on certain categories of nutrients (vitamins / fibers / etc...), we will check that the nutrients that we plan on using contain enough nutritive value using this database:

The dataset can be found here: [USDA Dataset](https://www.ars.usda.gov/northeast-area/beltsville-md-bhnrc/beltsville-human-nutrition-research-center/food-surveys-research-group/docs/fndds-download-databases/)


Let's take a look at the database.



<style  type="text/css" >
</style><table id="T_6f7d7376_2324_11ea_8a9e_0c5415885990" ><thead>    <tr>        <th class="blank level0" ></th>        <th class="col_heading level0 col0" >name</th>        <th class="col_heading level0 col1" >value</th>        <th class="col_heading level0 col2" >item</th>    </tr></thead><tbody>
                <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row0" class="row_heading level0 row0" >0</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row0_col0" class="data row0 col0" >Protein</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row0_col1" class="data row0 col1" >88.32</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row0_col2" class="data row0 col2" >ingredient    Soy protein isolate
nutrient                  Protein
value                       88.32
Name: 112450, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row1" class="row_heading level0 row1" >1</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row1_col0" class="data row1 col0" >Total Fat</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row1_col1" class="data row1 col1" >100</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row1_col2" class="data row1 col2" >ingredient    Fat, beef tallow
nutrient             Total Fat
value                      100
Name: 23791, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row2" class="row_heading level0 row2" >2</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row2_col0" class="data row2 col0" >Carbohydrate</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row2_col1" class="data row2 col1" >100</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row2_col2" class="data row2 col2" >ingredient    Sweetener, herbal extract powder from Stevia leaf
nutrient                                           Carbohydrate
value                                                       100
Name: 140012, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row3" class="row_heading level0 row3" >3</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row3_col0" class="data row3 col0" >Energy</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row3_col1" class="data row3 col1" >902</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row3_col2" class="data row3 col2" >ingredient    Fat, beef tallow
nutrient                Energy
value                      902
Name: 23793, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row4" class="row_heading level0 row4" >4</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row4_col0" class="data row4 col0" >Water</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row4_col1" class="data row4 col1" >99.98</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row4_col2" class="data row4 col2" >ingredient    Water, bottled, generic
nutrient                        Water
value                           99.98
Name: 103030, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row5" class="row_heading level0 row5" >5</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row5_col0" class="data row5 col0" >Fiber, total dietary</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row5_col1" class="data row5 col1" >53.2</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row5_col2" class="data row5 col2" >ingredient    Spices, curry powder
nutrient      Fiber, total dietary
value                         53.2
Name: 10669, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row6" class="row_heading level0 row6" >6</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row6_col0" class="data row6 col0" >Iron</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row6_col1" class="data row6 col1" >123.6</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row6_col2" class="data row6 col2" >ingredient    Spices, thyme, dried
nutrient                      Iron
value                        123.6
Name: 11646, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row7" class="row_heading level0 row7" >7</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row7_col0" class="data row7 col0" >Calcium</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row7_col1" class="data row7 col1" >7364</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row7_col2" class="data row7 col2" >ingredient    Leavening agents, baking powder, double-acting...
nutrient                                                Calcium
value                                                      7364
Name: 126435, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row8" class="row_heading level0 row8" >8</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row8_col0" class="data row8 col0" >Vitamin C</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row8_col1" class="data row8 col1" >2400</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row8_col2" class="data row8 col2" >ingredient    Fruit-flavored drink, powder, with high vitami...
nutrient                                              Vitamin C
value                                                      2400
Name: 172798, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row9" class="row_heading level0 row9" >9</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row9_col0" class="data row9 col0" >Vitamin B-6</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row9_col1" class="data row9 col1" >12</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row9_col2" class="data row9 col2" >ingredient    Cereals ready-to-eat, KELLOGG, KELLOGG'S ALL-B...
nutrient                                            Vitamin B-6
value                                                        12
Name: 44557, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row10" class="row_heading level0 row10" >10</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row10_col0" class="data row10 col0" >Vitamin B-12</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row10_col1" class="data row10 col1" >83.13</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row10_col2" class="data row10 col2" >ingredient    Beef, variety meats and by-products, liver, co...
nutrient                                           Vitamin B-12
value                                                     83.13
Name: 92334, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row11" class="row_heading level0 row11" >11</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row11_col0" class="data row11 col0" >Vitamin A, RAE</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row11_col1" class="data row11 col1" >9442</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row11_col2" class="data row11 col2" >ingredient    Beef, variety meats and by-products, liver, co...
nutrient                                         Vitamin A, RAE
value                                                      9442
Name: 92255, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row12" class="row_heading level0 row12" >12</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row12_col0" class="data row12 col0" >Vitamin E (alpha-tocopherol)</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row12_col1" class="data row12 col1" >149.4</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row12_col2" class="data row12 col2" >ingredient                 Oil, wheat germ
nutrient      Vitamin E (alpha-tocopherol)
value                                149.4
Name: 24853, dtype: object</td>
            </tr>
            <tr>
                        <th id="T_6f7d7376_2324_11ea_8a9e_0c5415885990level0_row13" class="row_heading level0 row13" >13</th>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row13_col0" class="data row13 col0" >Vitamin D (D2 + D3)</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row13_col1" class="data row13 col1" >10000</td>
                        <td id="T_6f7d7376_2324_11ea_8a9e_0c5415885990row13_col2" class="data row13 col2" >ingredient    Vitamin D as ingredient
nutrient          Vitamin D (D2 + D3)
value                           10000
Name: 177409, dtype: object</td>
            </tr>
    </tbody></table>



Obviously the dataset is biased by processed and enriched food which are made to contain more nutrients than "raw" foods. We will only focus on non-processed foods.



We will only take a look at beef and chicken for clarity purposes. We will also only consider raw meat as the cooking process alters the nutrient values. We are going to average the different categories of raw meat we are interested in (e.g. breasts and legs for chicken, different fat contents for beef).



<style  type="text/css" >
    #T_2fe6f314_2327_11ea_b3bc_0c5415885990 table {
          border-collapse: separate;
          border-spacing: 100px 500px;
    }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row0_col1 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row0_col2 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row1_col1 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row1_col2 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row2_col1 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row2_col2 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row3_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row3_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row4_col1 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row4_col2 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row5_col1 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row5_col2 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row6_col1 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row6_col2 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row7_col1 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row7_col2 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row8_col1 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row8_col2 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row9_col1 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row9_col2 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row10_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row10_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row11_col1 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row11_col2 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row12_col1 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row12_col2 {
            background-color:  #fee3d6;
            color:  #000000;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row13_col1 {
            background-color:  #e32f27;
            color:  #f1f1f1;
        }    #T_2fe6f314_2327_11ea_b3bc_0c5415885990row13_col2 {
            background-color:  #fee3d6;
            color:  #000000;
        }</style><table id="T_2fe6f314_2327_11ea_b3bc_0c5415885990" ><thead>    <tr>        <th class="col_heading level0 col0" >nutrient</th>        <th class="col_heading level0 col1" >Chicken Value</th>        <th class="col_heading level0 col2" >Beef Value</th>    </tr></thead><tbody>
                <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row0_col0" class="data row0 col0" >Calcium</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row0_col1" class="data row0 col1" >5.66667</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row0_col2" class="data row0 col2" >24</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row1_col0" class="data row1 col0" >Carbohydrate</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row1_col1" class="data row1 col1" >0.0833333</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row1_col2" class="data row1 col2" >0</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row2_col0" class="data row2 col0" >Energy</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row2_col1" class="data row2 col1" >149.667</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row2_col2" class="data row2 col2" >193.333</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row3_col0" class="data row3 col0" >Fiber, total dietary</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row3_col1" class="data row3 col1" >0</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row3_col2" class="data row3 col2" >0</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row4_col0" class="data row4 col0" >Iron</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row4_col1" class="data row4 col1" >0.463333</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row4_col2" class="data row4 col2" >1.83833</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row5_col0" class="data row5 col0" >Protein</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row5_col1" class="data row5 col1" >19.78</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row5_col2" class="data row5 col2" >17.5</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row6_col0" class="data row6 col0" >Total Fat</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row6_col1" class="data row6 col1" >7.41</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row6_col2" class="data row6 col2" >13.115</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row7_col0" class="data row7 col0" >Vitamin A, RAE</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row7_col1" class="data row7 col1" >14.3333</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row7_col2" class="data row7 col2" >3.33333</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row8_col0" class="data row8 col0" >Vitamin B-12</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row8_col1" class="data row8 col1" >0.34</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row8_col2" class="data row8 col2" >2.04333</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row9_col0" class="data row9 col0" >Vitamin B-6</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row9_col1" class="data row9 col1" >0.639667</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row9_col2" class="data row9 col2" >0.290833</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row10_col0" class="data row10 col0" >Vitamin C</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row10_col1" class="data row10 col1" >0</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row10_col2" class="data row10 col2" >0</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row11_col0" class="data row11 col0" >Vitamin D (D2 + D3)</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row11_col1" class="data row11 col1" >0.0333333</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row11_col2" class="data row11 col2" >0.0833333</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row12_col0" class="data row12 col0" >Vitamin E (alpha-tocopherol)</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row12_col1" class="data row12 col1" >0.32</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row12_col2" class="data row12 col2" >0.156667</td>
            </tr>
            <tr>
                                <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row13_col0" class="data row13 col0" >Water</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row13_col1" class="data row13 col1" >71.9867</td>
                        <td id="T_2fe6f314_2327_11ea_b3bc_0c5415885990row13_col2" class="data row13 col2" >68.745</td>
            </tr>
    </tbody></table>



We can see that chicken is lacking the Calcium, Iron and Vitamin B-12 when compared to beef. Therefore we would need to find a complementary substitute to replace beef with chicken. Fiber and Vitamin C are contained within crops and should not be considered here.



Milk is a good substitute for Calcium.


Granola is made from different cereals (here: wheat) and oats and is a good substitute for Iron deficiencies. Lentils are another good substitute. It is harder to find Vitamin B-12 ingredients that could replace beef.


It will be hard to replace the Vitamin B-12 found in beef-based diets, but there are alternatives (fish, game meat, chicken liver).
Overall we have seen that it is viable to replace beef consumption over the world from a nutrition and diet point of view.




<style  type="text/css" >
    #T_44df40e8_2327_11ea_b012_0c5415885990 table {
          border-collapse: separate;
          border-spacing: 100px 500px;
    }    #T_44df40e8_2327_11ea_b012_0c5415885990row0_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row0_col2 {
            background-color:  #ffece3;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row0_col3 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row1_col1 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row1_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row1_col3 {
            background-color:  #fc8e6e;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row2_col1 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row2_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row2_col3 {
            background-color:  #fb7252;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row3_col1 {
            background-color:  #fee7db;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row3_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row3_col3 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row4_col1 {
            background-color:  #ffeee7;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row4_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row4_col3 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row5_col1 {
            background-color:  #fee1d3;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row5_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row5_col3 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row6_col1 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row6_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row6_col3 {
            background-color:  #fed8c7;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row7_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row7_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row7_col3 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row8_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row8_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row8_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row9_col1 {
            background-color:  #fc9474;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row9_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row9_col3 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row10_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row10_col2 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row10_col3 {
            background-color:  #fee2d5;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row11_col1 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row11_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row11_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row12_col1 {
            background-color:  #fb694a;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row12_col2 {
            background-color:  #fff5f0;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row12_col3 {
            background-color:  #fc8767;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row13_col1 {
            background-color:  #fff1ea;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row13_col2 {
            background-color:  #fb6b4b;
            color:  #000000;
        }    #T_44df40e8_2327_11ea_b012_0c5415885990row13_col3 {
            background-color:  #fff5f0;
            color:  #000000;
        }</style><table id="T_44df40e8_2327_11ea_b012_0c5415885990" ><thead>    <tr>        <th class="col_heading level0 col0" >nutrient</th>        <th class="col_heading level0 col1" >Rice Value</th>        <th class="col_heading level0 col2" >Potato Value</th>        <th class="col_heading level0 col3" >Lentils Value</th>    </tr></thead><tbody>
                <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row0_col0" class="data row0 col0" >Calcium</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row0_col1" class="data row0 col1" >9</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row0_col2" class="data row0 col2" >12</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row0_col3" class="data row0 col3" >35</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row1_col0" class="data row1 col0" >Carbohydrate</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row1_col1" class="data row1 col1" >76.25</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row1_col2" class="data row1 col2" >17.49</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row1_col3" class="data row1 col3" >63.35</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row2_col0" class="data row2 col0" >Energy</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row2_col1" class="data row2 col1" >367</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row2_col2" class="data row2 col2" >77</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row2_col3" class="data row2 col3" >352</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row3_col0" class="data row3 col0" >Fiber, total dietary</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row3_col1" class="data row3 col1" >3.6</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row3_col2" class="data row3 col2" >2.1</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row3_col3" class="data row3 col3" >10.7</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row4_col0" class="data row4 col0" >Iron</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row4_col1" class="data row4 col1" >1.29</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row4_col2" class="data row4 col2" >0.81</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row4_col3" class="data row4 col3" >6.51</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row5_col0" class="data row5 col0" >Protein</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row5_col1" class="data row5 col1" >7.54</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row5_col2" class="data row5 col2" >2.05</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row5_col3" class="data row5 col3" >24.63</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row6_col0" class="data row6 col0" >Total Fat</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row6_col1" class="data row6 col1" >3.2</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row6_col2" class="data row6 col2" >0.09</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row6_col3" class="data row6 col3" >1.06</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row7_col0" class="data row7 col0" >Vitamin A, RAE</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row7_col1" class="data row7 col1" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row7_col2" class="data row7 col2" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row7_col3" class="data row7 col3" >2</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row8_col0" class="data row8 col0" >Vitamin B-12</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row8_col1" class="data row8 col1" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row8_col2" class="data row8 col2" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row8_col3" class="data row8 col3" >0</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row9_col0" class="data row9 col0" >Vitamin B-6</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row9_col1" class="data row9 col1" >0.477</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row9_col2" class="data row9 col2" >0.298</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row9_col3" class="data row9 col3" >0.54</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row10_col0" class="data row10 col0" >Vitamin C</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row10_col1" class="data row10 col1" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row10_col2" class="data row10 col2" >19.7</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row10_col3" class="data row10 col3" >4.5</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row11_col0" class="data row11 col0" >Vitamin D (D2 + D3)</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row11_col1" class="data row11 col1" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row11_col2" class="data row11 col2" >0</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row11_col3" class="data row11 col3" >0</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row12_col0" class="data row12 col0" >Vitamin E (alpha-tocopherol)</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row12_col1" class="data row12 col1" >0.6</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row12_col2" class="data row12 col2" >0.01</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row12_col3" class="data row12 col3" >0.49</td>
            </tr>
            <tr>
                                <td id="T_44df40e8_2327_11ea_b012_0c5415885990row13_col0" class="data row13 col0" >Water</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row13_col1" class="data row13 col1" >11.8</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row13_col2" class="data row13 col2" >79.25</td>
                        <td id="T_44df40e8_2327_11ea_b012_0c5415885990row13_col3" class="data row13 col3" >8.26</td>
            </tr>
    </tbody></table>



We can see that while potatoes are not a good enough nutrition substitute, lentils are a good substitute. 
Therefore it is reasonable to say that rice and beef can be compensated for by other meats or crops from a nutritional standpoint.
From an environmental impact perspective, it would be useful to reduce beef and rice production, and replace them by less GHG-intensive cultures.
