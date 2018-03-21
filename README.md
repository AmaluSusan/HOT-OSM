# Humanitarian OpenStreetMap
This is the reusable visualisation of NGOs in India using HOT OSM.
It contains selected Non-Governmental Organisations present within India that have been extracted and displayed with the help of Mapbox GL.

**Prerequisites**

1. In order to Extract data for map, the following set of commands are followed and for downloading mbtiles of various         countries(paste following link):

         https://osmlab.github.io/osm-qa-tiles/country.html

2. Commands to be pasted to terminal to get started:
  
       wget (link to india.mbtiles)

       sudo apt-get update

       sudo apt-get install git-core

       git  --version

       git clone https://github.com/mapbox/osm-tag-stats.git

       cd osm-tag-stats

       <sudo> npm install

       <sudo> npm link  

3. Now create a json file named [filter.json](https://github.com/AmaluSusan/HOT-OSM/blob/master/filter1.json) and save it in the    folder that containes the mbtiles file of the country.

4. To unzip the country.mbtiles file run the command:
       
       gunzip india.mbtiles.gz

5. To extract data enter the following command:
       
       osm-tag-stats --geojson=results.geojson --mbtiles="country.mbtiles" --filter='filter.json' –count


  After the extraction, a new file [results.geojson](https://github.com/AmaluSusan/HOT-OSM/blob/master/results.geojson?short_path=e7ccb58) will be automatically created in the folder with the extracted data.

6. Now create an HTML file, index.html including the details of the extracted information in results.geojson file.

 For building the HTML file you can take inspiration and learn more from
[Mapbox](https://www.mapbox.com/mapbox-gl-js/example/simple-map/)


**Visualised Map**

The map with the visualisation of NGOs can be viewed [here](https://AmaluSusan.github.io)

  

