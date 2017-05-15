
# Mapping review


*demo #1:* This map of counties for the entire US is modified slightly from Mike Bostock's [U.S. Topojson](https://bl.ocks.org/mbostock/410820) block. And the data from census.gov have been prepared differently.

* Demo: https://umbcvis.github.io/classes/class-14/index.html
* Review topics:
   * Geographies with [d3-geo](https://github.com/d3/d3-geo)
   * [projections](https://github.com/d3/d3/blob/master/API.md#projections)
   * [d3.geoPath](https://github.com/d3/d3-geo/blob/master/README.md#paths)
   * [topojson.feature](https://github.com/topojson/topojson-client/blob/master/README.md#feature) converts [TopoJSON](https://github.com/topojson/topojson) to [GeoJSON](http://geojson.org/)
   * [d3-selection](https://github.com/d3/d3/blob/master/API.md#selections-d3-selection)
       * joining data with ```selection.data()```
       * get the enter selection with ```selection.enter()``` (placeholders for data with no element)
       * append an element with ```selection.append()```

*demo #2:* This map shows only the counties in New York. It adds an interactive component that presents data from a second file containing population data. Run your mouse over the counties.

* Demo: https://umbcvis.github.io/classes/class-14/index2.html
* Review topics:
    * filter an array of GeoJSON objects
    * recenter a map using ```projection.fitExtent```
    * extract and display metadata properties in a GeoJSON object

*demo #3:* This map adds a threshold color scale to create a chloropleth map of population density.

* Demo: https://umbcvis.github.io/classes/class-14/index2.html
* Review topics:
    * data-dependent styling
    * color scales
    * event-driven styling
