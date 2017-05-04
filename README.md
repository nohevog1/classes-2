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
* [Class #4](https://github.com/umbcvis/classes/tree/master/class-03) -- Earthquakes for the entire US
    * USGS real-time earthquake feed
    * Add GeoJSON dots to a map
    * [d3-request](https://github.com/d3/d3/blob/master/API.md#requests-d3-request)
        * d3.json() -- get a JSON file
    * [topojson-client](https://github.com/topojson/topojson-client/blob/master/README.md)
        * Convert topology to GeoJSON
        * [topojson.feature(topology, object)](https://github.com/topojson/topojson-client/blob/master/README.md#feature)
