
# For Maryland, FIPS = 24
FIPS=24
FILE1=cb_2014_$(FIPS)_tract_500k
FILE2=cb_2014_$(FIPS)_tract_B01003

# Download and convert cenus-tract polygons
tracts.json: node_modules/shapefile
	curl 'https://www2.census.gov/geo/tiger/GENZ2014/shp/$(FILE1).zip' -o $(FILE1).zip
	# unzip the archive
	unzip -o $(FILE1).zip
	# convert to GeoJSON (also reads dbf file and adds feature.properties to the GeoJSON
	node_modules/shapefile/bin/shp2json $(FILE1).shp -o $@

# Download population from API (https://www.census.gov/developers/)
#  In this case, B01003_001 denotes total population estimate, "for" & "in" denote sampling
#  For detail, see API docs: https://www.census.gov/data/developers/data-sets/acs-5year.html
$(FILE2).json:
	curl 'https://api.census.gov/data/2014/acs5?get=B01003_001E&for=tract:*&in=state:'$(FIPS) -o $@

