## Final assignment

**Aim of the exercise**

In the final assignment you can put some of your new skills to the test. The objective of this assignment option is to acquire a rough overview of the potential impact of floods in the area around the town [Beledweyne]( https://en.wikipedia.org/wiki/Beledweyne) in Somalia. The town was hit by [floods in 2020]( https://reliefweb.int/disaster/ff-2020-000055-som). Now there are [elaborated plans on flood protection]( https://reliefweb.int/sites/reliefweb.int/files/resources/Urban%20Resilience%20Plan.pdf) in place. 

You will create a map which shows farmland and residential areas that are potentially effected by flooding of the [Shebelle river]( https://en.wikipedia.org/wiki/Shebelle_River). You can also check if facilities like schools and hospitals are potentially affected. 

Note that this is not a precise flood risk map, this is just an exercise!

[**Some inspiration**]( https://unosat-maps.web.cern.ch/SO/FL20200428SOM/UNOSAT_A3_Natural_Landscape_FL20200428SOM_Beledweyne_Somalia_13052020.pdf) 

**Data:**

Download the [final_assignment_data.zip](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/blob/main/Final%20assignment/final_assignment_data.zip) and save it on your PC. Create a local folder and save the above data there (remember that .zip folders must be unzipped).


- [Webi Shabeelle river)](https://data.humdata.org/dataset/hotosm_som_waterways) (Line) 
- Area of interest (Own data/ Polygone)
- Beledweyne landuse (OSM export) (Polygones)
- [Somalia health](https://data.humdata.org/dataset/hotosm_som_health_facilities) (polygones)
- [Somalia airports](https://data.humdata.org/dataset/hotosm_som_airports) (Points/ Polygones)
- [Somalia Leone roads](https://data.humdata.org/dataset/hotosm_som_roads) - [Info](https://wiki.openstreetmap.org/wiki/Key:highway) (Line)

**Note that you can also choose to only show a smaller part of the area of intrest if you like**

**Tasks**
1. Load the river, the area of interest and landuse data into your QGIS.
2. **(Optional)** You can add satellite imagery as base map via the [QuickMapServices](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Basemaps) plugin.
3. Make sure that all layers are projected in [Afgooye / UTM zone 38N (EPSG:20538)]( https://epsg.io/20538).
4. Classify the landuse data in useful manner.
5. Create one or multiple buffers around the river. Choose a reasonable extend of the buffers to identify potentially by floods effected areas around the river. 
6. Use the intersection tool to create a layer of potentially by floods effected farmland and residential areas based on the landuse data and the buffer(s).  
7. Load the health infrastructure and airports your QGIS and visualize them. If you chouse to show a large part of the area of interest in your final map you should create a point layer for the hospitals to visualize them better.
8. Load the road network in your QGIS. Decide which road types you want to show and only visualize these. Ask yourself which roads would be important in case of mayor floods in the area.
7. Create a map with all formal components (autor, date, scale,..) which shows the different kinds of landuse in the area of interest. Furthermore, the map should emphasize which areas are potentially at risk of flooding. 
8. Export your map as PDF and send it to... 


