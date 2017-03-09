# Earthquakes for the entire US

### Oklahoma earthquakes (from class 2)

* the code: http://github.com/umbcvis/classes/tree/master/class-02

* the demo: https://umbcvis.github.io/classes/class-02/

### US States (from class 3)

* https://umbcvis.github.io/classes/class-03/states.html

* Topojson reference docs: https://github.com/topojson/topojson

## The combination, created as follows...

1. Start with http://github.com/umbcvis/classes/tree/master/class-03/states.html
2. Log in to your github account and create a new gist by browsing to https://gist.github.com
3. Copy and paste the code into a file named "index.html" that you add to your gist
4. Add another file named "README.md" and type an interesting sentence.
4. Open your gist in blocks.org -- it should be the latest one at http://bl.ocks.org/your-github-username
5. Make necessary modifications to end up with http://github.com/umbcvis/classes/tree/master/class-03/states.html
   * Add a new "layer" -- a "g" element -- for drawing the earthquakes
   * Add the function that plots the earthquakes (on layer 2)

        function plotQuakes(error, json) {
          if (error) return console.log(error);

          // Global variable, data, will be visible in the console
          data = json;

          // Extract an array of feature objects, one for each earthquake
          var features = json.features;

          // Plot the earthquakes
          layer2.selectAll("path.quake")
              .data(features)
            .enter().append("path")
              .attr("class", "quake")
              .attr("d", path)
        }

   * Add the code to reads earthquakes and calls the function that plots them

        // Read and plot the earthquake data
        var usgs = "https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson";
        d3.json(usgs, plotQuakes);

6. The final code is in this gist:

https://bl.ocks.org/pbogden/eb4cafea0a3087fc1c2219c153dd2c63
