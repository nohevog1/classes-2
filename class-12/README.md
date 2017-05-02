# Chloropleth

Browser-based implementation of Mike Bostock's most excellent [Command-line Cartogaphy](https://medium.com/@mbostock/command-line-cartography-part-1-897aa8f8ca2c)

* demo: https://umbcvis.github.io/classes/class-12

The demo reproduces the Bostock's workflow for Maryland, and visualizes results for census tracts. If you open the developer console, you can inspect the data and see that the properties for each census tract includes FIPS code for the county.  These can be used for various purposes.  

For example, this demo uses the census tract FIPS code to remove all counties except the county with FIPS id = 003.

* demo #2: https://umbcvis.github.io/classes/class-12/county.html

If you look at the code, you'll see that the two demos differ in 2 sections. This one, which removes all tracts except those from a single county:

    // Remove all counties except the county with FIPS code = 003
    svg.selectAll('path.tract')
        .filter(function(d) { return d.properties.COUNTYFP !== "003" })
        .remove();

and another section that plots a single county boundary merged from its census tracts:

    // Get all tracts in the county with FIPS = '003'
    county = json.objects.tracts.geometries
        .filter(function(d) { return d.properties.COUNTYFP === '033'; });

    // Plot the boundry of the county with FIPS = "003"
    svg.append("path")
        .datum(topojson.merge(json, county))
        .attr('class', 'county')
        .attr('d', path)
        .style('stroke', '#aaa')
        .style('stroke-width', '2px')
        .style('fill', 'none');

* demo #3: https://umbcvis.github.io/classes/class-12/counties.html

This version of Mike Bostock's [US Counties Topojson](https://bl.ocks.org/mbostock/4122298) has one added line. On mouseover, it logs the county ID to the developer console.  The ID is a string representing the state FIPS (first two characters) and the county FIPS (characters 3-5).
