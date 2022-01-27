***Final assignment***

**Aim of the exercise**

In the final assignment you can put some of your new skills to the test. The objective of this assignment option is to acquire a rough overview of the potential impact of floods in the area around the town [Beledweyne]( https://en.wikipedia.org/wiki/Beledweyne) in Somalia. The town was hit by [floods in 2020]( https://reliefweb.int/disaster/ff-2020-000055-som). Now there are [elaborated plans on flood protection]( https://reliefweb.int/sites/reliefweb.int/files/resources/Urban%20Resilience%20Plan.pdf) in place. 

You will create a map which shows farmland and residential areas that are potentially effected by flooding of the [Shebelle river]( https://en.wikipedia.org/wiki/Shebelle_River). You can also check if facilities like schools and hospitals are potentially affected. 

Note that this is not a precise flood risk map, this is just an exercise!

[**Some inspiration**]( https://unosat-maps.web.cern.ch/SO/FL20200428SOM/UNOSAT_A3_Natural_Landscape_FL20200428SOM_Beledweyne_Somalia_13052020.pdf) 

**Data:**

Download the [final_assignment_data.zip](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/blob/main/Final%20assignment/final_assignment_data.zip) and save it on your PC. Create a local folder and save the above data there (remember that .zip folders must be unzipped).


- [Webi Shabeelle river)](https://data.humdata.org/dataset/hotosm_som_waterways) (Line) 
- Area of interest (Polygone)
- Beledweyne landuse (OSM export) (Polygone)
- Optional [Somalia health](https://data.humdata.org/dataset/hotosm_som_health_facilities) 
- Optional [Somalia airports](https://data.humdata.org/dataset/hotosm_som_airports) 
- Optional [Somalia Leone roads](https://data.humdata.org/dataset/somalia-roads) - [Info](https://wiki.openstreetmap.org/wiki/Key:highway)

**Tasks**
1. Load the data into your QGIS.
2. Make sure that all layers are projected in [Afgooye / UTM zone 38N (EPSG:20538)]( https://epsg.io/20538).
3. Classify the landuse data.
4. **(Optional)** You can use satellite imagery as base map via the [QuickMapServices](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Basemaps) plugin.
5. Create a buffer around the river. Choose a reasonable extend of the buffer.
6. Copy the part of the landuse layer which are potentially effected by flood with the [intersection tool](https://www.youtube.com/watch?v=QBVv7h2Jhvo)(Minute 02:05-02:25).
7. Create a map to visualize the landuse in the area and which areas are at risk of floods. Note that you can also choose to only show a smaller part of the area if you like. 
8. Export your map as PDF and send it to... 


