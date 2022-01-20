# Exercise Day 3

### Aim of the exercise
Repetition of some of Wednesday course contents.
Familiarization with the different kinds of (non)spatial analyses and geoprocessing tools.
Learning how to reveal circumstances and connections between spatial data features.

### Wiki:
* [Non spatial Joins](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/non-spatial-joins)
* [Table Functions](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/table-functions)
* [Spatial Queries](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Spatial-queries)
* [Geoprocessing Tools-Selection](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Geoprocessing-tools)
* [Non spatial queries](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/non-spatial-queries)
* [Classification of data](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Classification-of-data)
* [Styling panel](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Styling-panel)
* [Map design](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/map-design)

### Data:
Download all the [data sets](Ex4_Data.zip) and save the folder on your PC and unzip the file. The zip folder includes:
- `sen_healthsites.shp` (and the other shapefiles): Senegal healthsites data from https://data.humdata.org/dataset/senegal-healthsites
- `sen_admbnda_adm1_1m_gov_ocha_20190426.shp` (and the other shapefiles): Senegal boundary data (Admin level 1) from https://data.humdata.org/dataset/senegal-administrative-boundaries
- `EO4SD_SAINT_LOUIS_FLOOD_2018.shp` (and the other shapefiles): Saint Louis flood extend data from https://wbwaterdata.org/dataset/saint-louis-senegal-flood-risk-map-esa-eo4sd-urban
- `DI_Stat924.xls`: Senegal Desinventar Sendai Data showing effects of disasters in Senegal regions from https://www.desinventar.net/DesInventar/profiletab.jsp?countrycode=sen
- `sen_admpop_adm1_2020.csv`: Senegal administrative level 1 (région) 2019 projection population statistics from https://data.humdata.org/dataset/senegal-population-statistics

*Hint: All files still have their original name. Feel free to change their names to make it easier to identify them.*

---

## Tasks

There are two different options of tasks that you can select. They do not build on each other, so feel free to start with 1 or 2. It might make sense to create an own projects for each option to avoid confusion of data layers. The projected coordinate system for Senegal is `EPSG:32628- WGS 84 / UTM zone 28N`

### Option 1
Create an overview of disaster effects in the different regions of Senegal. Use non-spatial joins, table functions and the lessons about “Symbology“ from the last session.

* Load the Senegal administrative boundary layer (shp),  the population per subnational unit  and the Desinventar Sendai Data of Sengal into QGIS.
* Make sure to project the dataset with the boundaries into UTM zone 28N.
* Conduct non-spatial joins. The join can be based on the regions which are listed in both datasets.
    * First add the total population of each admin area to the shapefiles. Choose a suited field name and field data type.
    * Then add the number of directly and indirectly affected people. Choose a suited field name and field data type.
* Use the table functions to calculate the relative number of population directly and indirectly affected in relation to the total population per region.
* Use the “Symbology“ to choose a color scheme to visualize the share of directly affected people in the different regions (Hint: "Categorized“).
    * Play around with different modes to find a useful color/categorization scheme for the visualization.
     → Which regions are more and which are less directly affected? Are there data gaps?
* Export the map as png (Hint: Project, Import/Export, Export map to Image).
* Repeat the previous step, however this time visualize the indirectly affected people in each region (Hint: „Categorized“, column „Indirectly affected“).
* What are the differences to the directly affected regions when you look at the previously exported map?

### Task Option 2
Assess the Healthsite distribution in Saint Louis:
* Load the healthsites data and boundary data into your QGIS project. Load OpenStreetMap as a background layer (Hint: XYZ via browser window or QuickMapServices plugin).
* Make sure that you get your data into a projected coordinate system.
* Select all health sites which are located within the region Saint Louis:
    * Select the region “Saint_Louis“ in the boundary layer.
    * Save the selection under the new name “Saint_Louis_region“ in an extra layer.
    * Use the „Select by location“ or „clip“ tool to select all health facilities within the „Saint_Louis“ layer. * Save the new selection under the new name „healthsites_Saint_Louis“ in an extra layer (Hint: right click layer, export, …).
* Visual exploration: In which areas do we find more/less health sites?

Investigate Flood Risk in Saint Louis. After the successful selection of all health sites in the Saint Louis region in the previous step, please load the flood extend layer of Saint Louis into QGIS:
* Add the flood extend layer as an extra layer.
* The layer does not cover the whole Saint Louis region, however it goes beyond Saint Louis in the north.
* Use the clip tool to clip the flood extend layer to the Saint Louis region (Hint: Input Saint Louis flood extend, „Saint_louis_region“ as overlay) to enable focusing on central Saint Louis.
* Save the selection as „Saint_Louis_flood_clipped“.

When you look into the attribute table of the „Saint_Louis_flood_clipped“ layer (column watertype), you will see that the layer includes flooded, non-flooded and waterbody areas. Visualize only the flooded areas and water bodies in the dataset:
* Go into „Symbology“ and change the first selection from "Single symbols“ to „Categorized“.
* Select the column “watertype“ and click “Classify“.
* Choose different colors for the water bodies and the flooded areas. Leave non-flooded unmarked or make sure to make the areas transparent (opacity = 0%).
* Visual exploration: Which areas are more and less prone to flooding?

Assess which health sites are prone to flood risk.
* Make use of the „Select by expression“ tool to select all flooded areas in the „Saint_Louis_flood_clipped“ layer (Hint: WATERTYPE = ‘FLOODED‘).
* Save the selection in a separate layer “Saint_Louis_flooded_areas“.
* You can remove the “Saint_Louis_flood_clipped“ layer to avoid confusion.
* Make use of the „Select by location“ tool to assess which health sites are prone to flooding (are located within the layer which was created in the previous step).
* Check the attribute table of the “healthsites“ layer for selected features. (One pharmacy and one hospital should be selected.)

Which health sites are located close to flood zones?
* Create buffers around the health sites in Saint Louis with a distance of 20 meters.
* Make use of the „Select by location“ tool to assess which buffers intersect with flood areas. (*Hint: By the latest at that stage, you will be reminded to reproject your layers ;-) Meaningful buffers can only be calculated in projected coordinate systems.)
* How many health sites are selected? Check the attribute table. There should be five pharmacies and one hospital in the selection.
* Feel free to play around with additional buffer distances.
