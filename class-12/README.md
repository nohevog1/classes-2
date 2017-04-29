# Chloropleth

Browser-based implementation of Mike Bostock's most excellent [Command-line Cartogaphy](https://medium.com/@mbostock/command-line-cartography-part-1-897aa8f8ca2c)

* demo: https://umbcvis.github.io/classes/class-12

The demo reproduces the Bostock's workflow for Maryland, and visualizes results for census tracts. If you open the developer console, you can inspect the data and see that the properties for each census tract includes FIPS code for the county.  These can be used for various purposes.  

For example, this demo uses the census tract FIPS code to remove all counties except the county with FIPS id = 003.

* demo #2: https://umbcvis.github.io/classes/class-12/counties.html

If you look at the code, you'll the two demos differ by only 4 lines:

    // Remove all counties except the county with FIPS code = 003
    svg.selectAll('path.tract')
        .filter(function(d) { return d.properties.COUNTYFP !== "003" })
        .remove();the only difference between the two demos
