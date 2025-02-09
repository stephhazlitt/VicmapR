# VicmapR 0.1.4
* Add `httr::stop_for_status()` in several places for mor einformative errors  
* Add a `check_geoserver()` function to test whether the geoserver is operatonal (tests added)  
* Add pkgdown favicons  

# VicmapR 0.1.3  
* Fixed issues relating to CRAN submission for version 0.1.2. They were:  
    - Link to the used webservices added to the description field of DESCRIPTION.
    - Used only undirected quotation marks in the description text. e.g. `sf` --> 'sf'
    - Added \value to .Rd files regarding exported methods and explain the functions results in the documentation. Missing Rd-tags were:
    - `\dontrun{}` replaced with with `\donttest{}` for examples requirying connection to WFS. WFS speeds may vary and in some cases examples could take > 5 seconds.  
* Edited github actions to only run on push for main/master and pull requests

# VicmapR 0.1.2
* Global variables for `:=`, `name`, `type` and `.` were included with `utils::globalVariables()`  
* `\dontrun{}` added to examples collecting or filtering data and `listLayers()`, as these took over 10 seconds in CRAN checks.  
* Improvements to github actions  

# VicmapR 0.1.1

* `options(vicmap.base_url)` now accepts other base wfs urls to be used instead of the Vicplan one (e.g. the BOM wfs: `options(vicmap.base_url = "http://geofabric.bom.gov.au/simplefeatures/ahgf_shcatch/wfs")`)  
* A vignette on how to use Vicmap has been added
* Enhanced documentation and references
* Specified that GDAL > 3.0.0 is required  
* Additional tests have been written
* Checks for CRAN Submission and automated pkgdown deployment on Github 

# VicmapR 0.1.0

* VicmapR now builds queries in a step-wise fashion through the use of a `vicmap_promise` class. Similar to how [bcdata](https://github.com/bcgov/bcdata) works 
* Generic functions like `filter`, `select`, `head` can be used to refine the query.
* Data is returned using `collect`
* No longer relying on the `ows4R` package
* Other supporting functions such as `feature_cols`, `feature_hits`, `show_query` exist to help refine a query

# VicmapR 0.0.0.9000

* Added a `NEWS.md` file to track changes to the package  
* Wrote functions for basic WFS querying of data names and fields (`listLayers` and `listFields`)  
* Wrote a function to download and read in spatial data from Vicmap as `sf` objects (`read_layer_sf`)  

