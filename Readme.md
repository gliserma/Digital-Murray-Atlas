# Digital Murray Atlas Project
In 1761, following the British conquest of Canada, a detailed and extensive survey was undertaken of the St. Lawrence River valley. In scholarship, this came to be known as the Murray Atlas, named after the military governor of Quebec who was in charge of the effort. 

This project here is a digitally processed version of the Murray Atlas that I created for my M.S. Thesis at the University of Southern California in 2018. It includes vector data that I manually created directly from digital scans of the original map sheets along with some additional vector data that I inferred from the maps such as political boundaries.

## Organization
The project files includes:
- Two geodatabases:
  - Murray_Atlas_Not_Georeferenced.gdb: The vector data in the first is spatially referenced according to the unadjusted map sheets, arranged according to an unadjusted version of the index map
  - Murray_Atlas_Georeferenced.gdb: The vector data in the second is spatially adjusted with control points to match our present understanding of the geography, as refracted through the 'NAD 1983 Great Lakes and St. Lawrence ALbers' projection.
  - n.b. Both geodatabases contain the control points used to enact the spatial transformation.
- /Scholarship: My M.S. Thesis documenting how I created the data as well as how I assessed its accuracy.
- /Transformation_Files: This includes a .txt file that can be used to perform a spatial adjustment using the x-y coordinates extracted from the control points. This would permit a user to enact a different type of spatial transformation using the same control points. This also includes a csv with attributes for the control points that can be joined the control points files.
- /Library_Archives_Canada_Materials: This includes catalogue information for the map sheets as well as a link to the where the digital scans can be downloaded.

## Requirements
- Esri's ArcGIS Desktop. I most recently edited the data with v10.8.1 but earlier versions will likely work as well.

## TODO:
- I will add some more layers that still need metadata to the geodatabases for example concerning parish descriptions.
- The spatially adjusted raster data perform poorly -- I might process them further to improve this situation.
- I want to develop a tool that will spatially adjust raster and vector data together, though this will likely be a separate project.