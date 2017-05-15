
# For New York, FIPS = 36
FIPS=36

all: counties.json population.json

node_modules:
	npm install shapefile
	npm install topojson

# Download population from Census.gov API (https://www.census.gov/developers/)
#  In this case, B01003_001 denotes total population estimate, "for" & "in" denote sampling
#  For detail, see API docs: https://www.census.gov/data/developers/data-sets/acs-5year.html
population.json:
	curl 'https://api.census.gov/data/2014/acs5?get=B01003_001E&for=county:*&in=state:'$(FIPS) -o $@

# Download and convert county polygons (available resolutions: 1:500k, 1:5m, 1:20m)
# See: https://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html
counties.json: node_modules
	curl -LO "http://www2.census.gov/geo/tiger/GENZ2014/shp/cb_2014_us_county_20m.zip" -o cb_2014_us_county_500k.zip
	# unzip the archive
	unzip -o cb_2014_us_county_20m.zip
	# convert to GeoJSON (also reads dbf file and adds feature.properties to the GeoJSON
	node_modules/shapefile/bin/shp2json cb_2014_us_county_20m.shp -o shape.json
	# convert to topojson
	node_modules/topojson/node_modules/.bin/geo2topo counties=shape.json > counties.json

clean:
	-rm cb*
	-rm shape.json
	-rm -r node_modules
