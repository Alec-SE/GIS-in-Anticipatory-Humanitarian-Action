# Exercise_5

### Aim of the exercise

Repetition of the OpenStreetMap download, vector data geprocessing and first analyses of raster data. 
Learning how to reveal circumstances and connections between vector and raster data features.

### Wiki:

- QuickOSM
- Buffer
- Open Raster Layer
- Reproject Raster (Warp)
- Zonal statistics


### Data:
[„per_ppp_2020_UNadj_constrained“](per_ppp_2020_UNadj_constrained.zip) from WorldPop https://www.worldpop.org/geodata/summary?id=50047

### Understand the state of the Healthcare coverage in the Cusco region (Peru)/ Background:

In scope oft he Covid response in 2020, the Humanitarian OpenStreetMap Team has mapped the entire Cusco region, home to 1.2 million people and with extremely varied terrain; from Altiplano communities living at 5,000m altitude to Amazonian jungle. Creating better maps has allowed government workers to begin using the data to assess healthcare needs. This is particularly vital for maternal healthcare services, which have been largely unavailable over the past few months due to quarantine.
Also see: https://www.forecast-based-financing.org/2020/09/24/anticipating-and-addressing-epidemics-the-potential-of-open-data-initiatives/
https://www.hotosm.org/updates/covid-19-pandemic-in-peru-mapping-health-implications/* 
In the exercise you will learn how to assess the population that is located in a 10 km distance of health facilities (here: hospitals and clinics).
Read through the whole exercise before you start with the first steps.

## Vector data analyses

* Download all hospitals and clinics in the “Cusco“ region using QuickOSM (look for the correct tags in the MapFeatures webpage). The result will be a polygon and a point layer (Hint: Wiki QuickOSM).

* Reproject both of the layers to EPSG:32719 - WGS 84 / UTM zone 19S and save them under new names.

* Create 10 kilometer buffers around both of the healthcare layers and make sure to mark „Dissolve result“ (Hint: Wiki Buffer). 

* Merge both datasets to one vector dataset using the „Merge Vector Layers“ Tool:

![](Merge_vector.png)

* Input: Select the „…“ and select both buffer layers as input. Save the created „Merged layer under a new file name.

![](select_buffer_layers.png)

* Merge the feature attributes in the layer by
1. Opening the attribute table
2. Toggle editing/ Start the editing mode
3. Select all attributes (only two rows in the attribute table in this example)
4. Go to the „Edit“ menu and select „Merge selected features“

![](Select_all_attributes.png)

5. Press okay to start the process.
6. Stop the editing process and save the changes (click „save“ when stop editing).

## Raster and vector data analyses

* Load the raster data set into QGIS (Hint: Wiki Raster). 

* Use the „Warp (Reproject)“ Tool to reproject the raster layer to UTM 19S (Hint: Wiki Raster).

* Zonal statistics (Hint: Wiki Raster):
1. Open the „Zonal statistics tool“
2. Select the merged buffer layer as vector input layer and the population layer as raster input 
3. Choose the statistics you would like to calculate (e.g. count, sum, mean)
4. Choose a folder for your output.
5. The „_sum“ column in the attribute table of the newly created layer provides information about the        population inside the selected „merge buffer layer“ area.

*Hint: 
If you would like to get statistics of the single layers, leave out the merge layer step and apply the zonal statistics to both vector layers seperately.
If you would like to create statistics for each buffer region, do not set the mark at „Dissolve result“.*

## ORS Tools

While the result of the previous steps show that quite a large part of the population seems to live not more than 10 kilometers from a health facility, the terrain around Cusco could have an important effect on the accessibility.

Select single health facilities and asssess how accessible they are using the ORS Tools (ORS Plugin, also see [Wiki ORS Tools](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/ORSTools))).

Feel free to play around with different times and distances.


