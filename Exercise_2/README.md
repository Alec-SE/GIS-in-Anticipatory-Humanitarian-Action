**Exercise 2**

In this scenario, we will create an overview map of the prevalence of stunting in Sierra Leone at the district level. For this reason, we will visualise both the prevalence of stunting and key infrastructure such as hospitals, airports and roads. The final decision on which data to visualise and in which way is up to you, the cartographer.  

**Aim of the exercise**

Gather first experiences with the visualization tools of QGIS.
Obtain the skills to produce a printable map with QGIS.
 

**Wiki:**

- [Basemaps](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/basemaps)
- [Classification of data](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Classification-of-data)
- [Styling panel](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Styling-panel)
- [Map design](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/map-design)


**Data:**

Download the [data]() and save it on your PC. Create a local folder and save the above data there. (.zip folders must be unzipped beforehand.)


- [Sierra Leone prevalence of stunting 2014 (data modified)](https://geonode.wfp.org/layers/geonode%3Asle_ica_malnutrition_geonode_20170517) (Polygons) 
- [Sierra Leone national boders](https://data.humdata.org/dataset/geoboundaries-admin-boundaries-for-sierra-leone) (lines)
- [Sierra Leone provinces](https://data.humdata.org/dataset/geoboundaries-admin-boundaries-for-sierra-leone) (Lines)
- [Sierra Leone health](https://data.humdata.org/dataset/sierra-leone-healthsites) (Points)
- [Sierra Leone airports](Sierra Leone airports) (Points) 
- Optional [Sierra Leone roads](https://data.humdata.org/dataset/hotosm_sle_roads) (lines)- [Info](https://wiki.openstreetmap.org/wiki/Key:highway)

**Tasks**
1. Open the above files in QGIS. Load the vector layers prevalence of stunting 2014, national boders, provinces and airports into your programme.
2. Classify the stunting data and adjust the coloring. See wiki [Classification of data- Classification of ordinal scaled data](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Classification-of-data)
3. (Optional) Load the health layer in QGIS. Classify the health layer to only show hospitals. ![]() 
3. Chose symbology and colors for borders, roads, hospitals and airports which seems fit to you. See wiki [Styling panel](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Styling-panel)
4. (Optional) Load the layer roads in QGIS. Classify the roads with the column "highway". Chose which roads and path you want to visualize and adjust a suitable symbology.
5. (Optional) Add a basemap to your map via the Plugin- QuickMapServices- Adjust the opacity of your layers to make the best use of the basemap. [Tutorial video]( https://www.youtube.com/watch?v=dTfCOlUxVbo)
6. Great a print layout and add features like title, sources, scales, legend and North arrow. See wiki [Map design](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/map-design) 
7. Export your map as PDF.



##This (or similar) is what it looks like in the end:
