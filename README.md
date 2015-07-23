# LEHD Mapping of job patterns in CT


## The map
Inspiration:   http://www.robertmanduca.com/projects/jobs.html

This a map the displays points for every job, classified by NAICS code (industry classification), as reported via the Census Longitudinal Employer-Household Dynamics dataset (LEHD). It is a catrographic style known as dot density. The census data is extracted at the block level. Points are generated based on the count of jobs in different categories and then randomly plotted within the block group polygon. The location is not a precise geographic location, but rather algorithmic, in order to display both the intensity of a phenomenon as well as the variation at the given geographic scale.

Here are some other examples and technical note:

http://indiemapper.com/app/learnmore.php?l=dot_density
http://www.coopercenter.org/demographics/Racial-Dot-Map
http://databurgh.tumblr.com/post/87006526454/building-a-scatterplot-map-in-qgis-and-tilemill


Alternatives include hex bin maps:

https://github.com/kevinschaul/binify
https://www.mapbox.com/blog/binning-alternative-point-maps/

Or just standard choropleth maps.

NAICS Code List: http://www.naics.com/search/

## The data

The LEHD data is quite rich. It is a model-based approach for estimating journey-to-work at the census block level. Using a variety of data sets (Department of Labor and Census), counts are generated for the home-work location of jobs, organized by job classification and other factors.

The map above represents this data only by looking at the location of jobs. Alternative views could be

- Mapping the job classification of workers by residential location
- Mapping the distance traveled by job location / type
- Mapping job classification by age, wage range, etc...
	- For example, do job locations of high wage vs. low wage professional service differ?
	- Are there geographic differences in the age distributions of workers in certain categories?
	- Etc.
- Break down of the aggregate categories (Manufacture & Trade, Professional Services, Healthcare/Ed/Government, Retail & Hospitality) in finer grain view
- Historic change views (2002-2012 data is available)

You can get a better feel for the possibilities of the data by poking around w/ the On The Map tool: http://onthemap.ces.census.gov/


## Next steps

- Explore the data and come up w/ a few differnet data scenarios
- Extract the LODES data: http://lehd.ces.census.gov/data/#lodes
	- Origin-Destination
	- Residence Area Characteristics (RAC)
	- Workplace Area Characteristics (WAC)
- Load into database and start writing queries to aggregate / extract datasets for mapping
- Develop map / interface design
- Develop
- Publish