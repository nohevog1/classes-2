# classes

A collection of demos for each class

* [Class #1](https://github.com/umbcvis/classes/tree/master/class-01) -- Use D3 to create a simple HTML bar chart
    * General layout of a document -- introduction to HTML, CSS, JavaScript
    * [d3-scale](https://github.com/d3/d3/blob/master/API.md#scales-d3-scale) -- Scales
        * Scales map data to a visual representation.
    * [d3-selection](https://github.com/d3/d3/blob/master/API.md#selections-d3-selection) -- Selections
        * Transform the DOM (Document Object Model) by selecting elements and joining them to data.
            * d3.scaleLinear() -- quantitative linear scale
        * Selecting elements
            * d3.select() -- select an element from the document
            * d3.selectAll() -- select multiple elements from the document
        * Modifying elements
            * selection.style() -- add a CSS attribute to the selection
            * selection.text() -- get or set the text content
        * Joining data
            * selection.data() -- join elements to data
            * selection.enter() -- the "enter" selection (data missing elements)
            * selection.exit() -- the "exit" selection (elements missing data)
            * selection.append() -- create, append and select new elements
    * Reading: [Let's Make a Bar Chart](https://bost.ocks.org/mike/bar) by Mike Bostock
* [Class #2](https://github.com/umbcvis/classes/tree/master/class-02) -- Oklahoma earthquakes
    * Introduction to SVG
    * Introduction to JSON, GeoJSON & TopoJSON
    * JavaScript -- Functions, Objects, Arrays
    * Developer (JavaScript) console -- inspecting data and JavaScript, debugging, testing, experimenting
* [Class #3](https://github.com/umbcvis/classes/tree/master/class-03) -- Three little circles
    * Demo: Practice with the developer console
    * Another demo: US State outlines from TopoJSON
    * Create and modify 3 little SVG circles with D3
    * Reading: [3 Little Circles](http://bost.ocks.org/mike/circles/) by Mike Bostock
* [Class #4](https://github.com/umbcvis/classes/tree/master/class-04) -- Earthquakes for the entire US
    * USGS real-time earthquake feed
    * Add GeoJSON dots to a map
    * [d3-geo](https://github.com/d3/d3/blob/master/API.md#geographies-d3-geo) -- Geographies
        * [d3.geoPath](https://github.com/d3/d3-geo/blob/master/README.md#geoPath) -- Geographic path generator
        * [d3.geoAlbersUsa, etc.](https://github.com/d3/d3/blob/master/API.md#projections) -- Built-in projections
    * [d3-geo-projection](https://github.com/d3/d3-geo-projection) -- Extended geographic projections
    * [d3-request](https://github.com/d3/d3/blob/master/API.md#requests-d3-request)
        * d3.json() -- get a JSON file
    * [topojson-client](https://github.com/topojson/topojson-client/blob/master/README.md)
        * Convert TopoJSON to GeoJSON
        * [topojson.feature(topology, object)](https://github.com/topojson/topojson-client/blob/master/README.md#feature)
* [Class #5](https://github.com/umbcvis/classes/tree/master/class-05) -- Earthquakes for the entire US II
    * Add a legend to the demo from Class #4
    * Data-dependent labels and colors
    * [d3.scaleOrdinal](https://github.com/d3/d3/blob/master/API.md#ordinal-scales) -- ordinal scales
    * [d3.schemeCategory10](https://github.com/d3/d3-scale/blob/master/README.md#schemeCategory10) -- categorical color scheme
* [Class #6](https://github.com/umbcvis/classes/tree/master/class-06) -- Scatterplot
    * Global earthquakes -- magnitude vs longitude
    * Exposing interesting features in the data (US has all the small earthquakes)
    * [d3.scaleSequential](https://github.com/d3/d3/blob/master/API.md#sequential-scales) -- sequential scales map continuous domain to an interpolator
    * [d3.interpolateRainbow](https://github.com/d3/d3-scale/blob/master/README.md#interpolateRainbow) -- continuous color scheme used as an interpolator
    * [d3-scale-chromatic](https://github.com/d3/d3-scale-chromatic) -- categorical & continuous color schemes
    * [Axes](https://github.com/d3/d3/blob/master/API.md#axes-d3-axis)
        * [d3.axisBottom](https://github.com/d3/d3-axis/blob/master/README.md#axisBottom) -- bottom-oriented axis
        * [d3.axisLeft](https://github.com/d3/d3-axis/blob/master/README.md#axisLeft) -- left-oriented axis
* Class #7 -- Review & Projects
* Class #8 -- Spring Break
* [Class #9](https://github.com/umbcvis/classes/tree/master/class-09) -- Raster & Vector I
    * Map tiles based on [OpenStreetMap](https://www.openstreetmap.org)
    * [d3-tile](https://github.com/d3/d3-tile) -- working with image-based map tiles
    * [d3-queue](https://github.com/d3/d3/blob/master/API.md#queues-d3-queue) -- managing asynchronous tasks
* [Class #10](https://github.com/umbcvis/classes/tree/master/class-10) -- Raster & Vector II (Slippy Map)
    * Global earthquakes on a slippy map
    * [d3-zoom](https://github.com/d3/d3/blob/master/API.md#zooming-d3-zoom) -- pan & zoom with mouse (or touch)
* [Class #11](https://github.com/umbcvis/classes/tree/master/class-11) -- Vector tiles
    * CSS styling of OSM data as vector tiles combined with earthquake data
* [Class #12](https://github.com/umbcvis/classes/tree/master/class-12) -- Chloropleth maps
    * "Command-line cartography" without the command line
    * [selection.filter](https://github.com/d3/d3/blob/master/API.md#selections-d3-selection) -- Filter elements based on data
    * [topojson.merge](https://github.com/topojson/topojson-client/blob/master/README.md#merge) -- Union of objects in a topology
        * Example: counties constructed from census tracts
    * Reading: [Command-line cartography](https://medium.com/@mbostock/command-line-cartography-part-1-897aa8f8ca2c) by Mike Bostock
* [Class #13](https://github.com/umbcvis/classes/tree/master/class-13) -- Drag a dot
    * [d3-drag](https://github.com/d3/d3/blob/master/API.md#dragging-d3-drag) -- Dragging
    * [drag events](https://github.com/d3/d3-drag#drag-events) -- In case you thought dragging was simple
    * [d3.event](https://github.com/d3/d3-selection#event) -- The current event, if any
    * [d3.mouse](https://github.com/d3/d3-selection#mouse) -- X & Y coordinates of the current event
    * [projection.invert](https://github.com/d3/d3/blob/master/API.md#projections) -- Unproject a point (to a sphere)
* [Class #14](https://github.com/umbcvis/classes/tree/master/class-14) -- Mapping review

* [Final exam template](http://bl.ocks.org/pbogden/5c09aa450bc9448cf65f3fcd52034113)

