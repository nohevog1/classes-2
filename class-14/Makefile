
# For New York, FIPS = 36
FIPS=36

all: population.json

# Download population from Census.gov API (https://www.census.gov/developers/)
#  In this case, B01003_001 denotes total population estimate, "for" & "in" denote sampling
#  For detail, see API docs: https://www.census.gov/data/developers/data-sets/acs-5year.html
population.json:
	curl 'https://api.census.gov/data/2014/acs5?get=B01003_001E&for=county:*&in=state:'$(FIPS) -o $@

