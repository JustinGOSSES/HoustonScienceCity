# Houston Science City Map

Current map is <a href="https://justingosses.github.io/HoustonScienceCity/">live</a> as a github.io page


## Purpose:
Exploration of the idea you could map out all the different places science is taught, applied, and created in Houston, thereby giving people a great appreciation of how pevarsive it is in their lives. 

### Current Github Location: 
https://github.com/JustinGOSSES/HoustonScienceCity.git

### Started the map from this example:
https://www.mapbox.com/mapbox-gl-js/example/toggle-layers/

## Methods Brainstorming:
1.Starting off using geojson from the city of Houston's <a href='http://cohgis-mycity.opendata.arcgis.com/' target="blank">open data GIS portal</a>. 

2. One possible way to find businesses that use science is to webscrape or a job website's API to search for all job advertisements over the last year that mention a word from a list of words for scientist. The next step would be to pull company names from those returns and use a google places API to find all the locations. Those latitudes could be plotted on the map with some of the meta data. There would be false positives, but it might work out alright?
	- Update: 
		- The google places API will work fairly well for an input of business name and city. There are some complications having to do with API responses being limited to 20 items, but that limit can be got around by constraining API calls to smaller areas of geography. 
			- Some good results were found using science related terms like 'laboratory' and 'oil and gas'. A decent number of results, perhaps in the hundreds, could be produced with a decent sized list of creative terms?
		- The job sites APIs are mostly closed it seems. Access is limited websites that would put their data or links on their page and provide clicks back to the original job search site. Web scaping using beautiful soup might be a more likely option?

- Another method would be to do a series of twitter API searches around the #reallivingscientist with the distance criteria of 10 or 20 kilometers and the centerpoint set to various zip code centerpoints. The data wouldn't be specific to an exact point but could at least be positioned at neighborhood level and could involved photos and text. 
	- This works well. It requires a bit more work on formatting into better organized json, compilation of multiple API calls into a single file, and then transformation into geoJSON to get it on the map. 


#### Original List of Potential Map Data:
- Houston science twitter handles?
- Job ad at this company mentioned science
- Actually a Scientist
- User provided information using google forms or google sheets, that then combines with other information
	-- lat/long
	-- Full street address with zip
	-- Name
	-- If government agency & type
	-- Type of science, multiple okay
	-- Website link
	-- How the organization or site or data matters to you or others
	-- In relation to this organization and their science work, are you worried about negative impact of funding reduction, censorship, or science not being used in policy?

- Schools, Houston region (no universities!) City data types: 
http://cohgis-mycity.opendata.arcgis.com/datasets/59d52cd8fa9d463ea7cf9f3c0a0c6ea2_0?geometry=-96.376%2C29.57%2C-94.399%2C29.927

- Muncipal Libraries - City data types: http://cohgis-mycity.opendata.arcgis.com/datasets/59d52cd8fa9d463ea7cf9f3c0a0c6ea2_12?geometry=-95.804%2C29.697%2C-94.815%2C29.876
- Museums (needs editing down to Science?) - City data types : http://cohgis-mycity.opendata.arcgis.com/datasets/59d52cd8fa9d463ea7cf9f3c0a0c6ea2_13
- Trauma Centers - City data types: http://cohgis-mycity.opendata.arcgis.com/datasets/59d52cd8fa9d463ea7cf9f3c0a0c6ea2_9
- Hospitals - city data types : http://cohgis-mycity.opendata.arcgis.com/datasets/59d52cd8fa9d463ea7cf9f3c0a0c6ea2_10
- Parks - city data types : http://cohgis-mycity.opendata.arcgis.com/datasets/59d52cd8fa9d463ea7cf9f3c0a0c6ea2_16?geometry=-95.883%2C29.684%2C-94.895%2C29.863
- Natural gas fields, http://www.commissionerbushmaps.com/
- Federal agencies?
- State agencies?
- County agencies?
- Local agencies?
- User suggested data?
- data.gov https://catalog.data.gov/dataset
- https://catalog.data.gov/dataset/college-scorecard
- dice job board API - http://www.dice.com/common/content/util/apidoc/jobsearch.html
- indeed API https://ads.indeed.com/jobroll/xmlfeed , meant for putting their widget on their site but might still work
- Various job APIs, a big list - https://www.programmableweb.com/news/70-jobs-apis-indeed-simply-hired-and-careerbuilder/2013/01/23
- Inside Higher Ed job API - https://www.programmableweb.com/api/inside-higher-ed
- Monster job search API - http://partner.monster.com/power-resume-search-devguide
- google places API - https://developers.google.com/places/web-service/search

### Early Map
![bad photo!]
(https://github.com/JustinGOSSES/HoustonScienceCity/blob/master/Images/earlyMap.png)
