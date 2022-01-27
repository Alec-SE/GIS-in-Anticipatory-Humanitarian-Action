**Final assignment**

**Aim of the exercise**

In the final assignment you can put some of your new skills to the test. The goal is to acquire a ruff overview of the potential impact of floods in the area around the town [Beledweyne]( https://en.wikipedia.org/wiki/Beledweyne) in Somalia. The town was hit by [floods in 2020]( https://reliefweb.int/disaster/ff-2020-000055-som). Now there are [elaborated plans on flood protection]( https://reliefweb.int/sites/reliefweb.int/files/resources/Urban%20Resilience%20Plan.pdf) in the area. 
You will great a map which shows farmland and residential areas which are potentially effected by floods of the [shebelle river]( https://en.wikipedia.org/wiki/Shebelle_River). You can also check if facility’s like schools and hospitals are also potentially affected. 
Note that this is not a precise flood risk map, this is just an exercise!

**Data:**

Download the [data (final_assignment_data)]() and save it on your PC. Create a local folder and save the above data there. (.zip folders must be unzipped beforehand.)


- [Webi Shabeelle river)](https://data.humdata.org/dataset/hotosm_som_waterways) (Line) 
- Area of interest (Polygone)
- Beledweyne landuse (OSM export) (Polygone)
- Optional [Somalia health](https://data.humdata.org/dataset/hotosm_som_health_facilities) 
- Optional [Somalia airports](https://data.humdata.org/dataset/hotosm_som_airports) 
- Optional [Somalia Leone roads](https://data.humdata.org/dataset/somalia-roads) - [Info](https://wiki.openstreetmap.org/wiki/Key:highway)

**Tasks**
1. Load the data into your programme.
2. Make sure that all layers are projected in [Afgooye / UTM zone 38N (EPSG:20538)]( https://epsg.io/20538).
3. Classify the landuse data.
4. **(Optional)** You can use stability imagery as base map via the [QuickMapServices](https://gitlab.com/Alec-SE/gis-in-anticipatory-humanitarian-action/-/wikis/Basemaps) plugin.
5. Great a buffer around the river. Chose a reasonable extend of the buffer.
6. Cut the party of the landuse layer which are potentially effected by flood with the intersection tool.
7. Great a map to visualize the landuse in the area and which areas are at risk of flood. Note that you can also chose to only show a smaller part of the area if you like. 
8. Export your map as PDF.


##This (or similar) is what it looks like in the end:

![]() 
