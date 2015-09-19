# Shapefiles

This is a repo that has shapefiles for some fun data sets, mostly downloaded
or collected from various GIS systems or people who work in local GIS systems.

This is meant to be a curated, streamlined list. For an archive and larger
selection of less common (or large) shapefiles, see: https://github.com/HackFargo/Shapefiles-Archive

The zip files contain the original shapefile, which can be loaded into
ArcGIS or other GIS systems. I've converted the shapefile into a GEOJson
format that can be used by a variety of libraries, including leaflet.js

The nice thing about github is that you can preview the GEOjson file in
the browser, which makes the data approachable and easy to understand.

In some cases, you may want to convert to TopoGSON (an extension of
GeoJSON), which will likely save you on space (up to 90%), at the expense of not
being as widely accepted by most libraries.

If you know how to download shapefiles directly from the city of fargo
or moorhead GIS systems, please write up a tutorial. It's not straight
forward by any means.

[Use this great GEOJson preview] for testing GeoJson files (it is a simple
leaflet.js example). More info on leaflet.js / [GeoJson here](http://leafletjs.com/examples/geojson.html).

If you would like to make your own GeoJSON files, it's easy. First, be 
sure to install the gdal package. On linux: ``` apt-get install gdal-bin ```

To convert a single shapefile:

``` bash
ogr2ogr -f GeoJSON -t_srs crs:84 FargoParks.geojson FargoParks.shp
```

There's also a nice [bash helper](https://gist.github.com/benbalter/5858851) for multiple files.

Other resources include:

  * [ND Data Portal](https://apps.nd.gov/hubdataportal/srv/en/main.home) which typically leads to the [ND GIS System](http://www.nd.gov/gis/apps/DataDownload/)
    -- this system is *awesome* and lets you download all kinds of state
    wide data sets (ecological, transportation, health, infrastructure).
    I wish every GIS system was like this because it makes grabbing data
    for downloading super easy.

  * City of Fargo GIS: http://gis.cityoffargo.gov

  * [Cass County ND GIS](https://www.casscountynd.gov/county/depts/GIS/download/Pages/shapefiles.aspx) -- another fantastic resource for 
    downloading data. They have a whole bunch of fun shape files for download.

  * [Clay County MN GIS](http://claycountymn.gov/658/GIS-Data) -- more files for download across the river

