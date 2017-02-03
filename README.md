devroadmap
==========

rOpenSci Development Road Map

This document does not track every project/package within rOpenSci,
but rather the larger efforts we are undertaking.

Go to Issues/Milestones for each respective package to get up
to date information on issues and planned release dates.

For past changes on a per pacakge basis: All rOpenSci repositories should
have notes on each release in the `releases` tab for
(e.g., [releases for rgbif](https://github.com/ropensci/rgbif/releases)). If
releases is missing see the `NEWS`/`NEWS.md` file in the repository.

--------

## To Do

### taxonomy

__target date: Mar 2017__

`taxize` is our core taxonomy package that's been around for years, and is used widely. We're targeting a [v1.0 release](https://github.com/ropensci/taxize/milestones/v1.0) for January 2017. Before that, along with a `v0.8` release of `taxize` (~ Aug/Sep) we can target first versions of `taxizedb` and `taxa` (with `binomen` folded in).

* [taxize](https://github.com/ropensci/taxize)
* [taxizedb](https://github.com/ropenscilabs/taxizedb) - use SQL dumps of taxonomic databases locally
* [binomen](https://github.com/ropensci/binomen) - dplyr like interface for taxonomic data __this will likely be merged with `taxa`__
* [taxa](https://github.com/ropenscilabs/taxa) - classes for taxonomic data - in the future to be used by all other taxonomy packages __waiting on this getting to CRAN, should be soonish__

### biodiversity data

__target date: Apr 2017__

Continual patch releases of these are put out, but we could target a single date to release new versions of a suite of these pkgs:

* [rgbif](https://github.com/ropensci/rgbif)
* [spocc](https://github.com/ropensci/spocc)
* [ecoengine](https://github.com/ropensci/ecoengine)
* [scrubr](https://github.com/ropenscilabs/scrubr)
* [mapr](https://github.com/ropensci/mapr)
* etc... there are more


## Completed

### infrastructure

We are working on a new system for massively concurrent requests in `curl` to support high performance scarpers and crawlers. Because this is a big update, it needs a few more rounds of tweaking and testing and revision.

* [curl](https://github.com/jeroenooms/curl)


### images and graphics

The new `magick` package opens up a lot of possibilities for advanced image processing in R. In July we have implemented the core foundations and fixed low-level problems to make the package work seamlessly on all platforms. In august we make R interfaces more user friendly and improve documenation.

* [magick](https://github.com/ropensci/magick)

Based on magick, we can derive other packages to work with animation and graphics post-processing (e.g. for journal publications). We can also tie this in with raster types for spatial applications.


### geospatial

J and S are working on `geojson`, a pkg for geojson classes, which we can use in other packages. We can pair this release with `geoops`, a package to do geospatial operations without the gdal/geos stack, and a new version of `geojsonio`, our geojson I/O client. We could include new release of `geojsonlint` if appropriate. Perhaps throw in `wellknown` if I can get around to updating it.

* [geojsonio](https://github.com/ropenscilabs/geojsonio)
* [geojson](https://github.com/ropenscilabs/geojson)
* [geoops](https://github.com/ropenscilabs/geoops)
* [geosonlint](https://github.com/ropenscilabs/geojsonlint)
* [wellknown](https://github.com/ropenscilabs/wellknown)
* Implement `geobuf` format (binary geojson) in [protolite](https://github.com/jeroenooms/protolite) - this is now done ✔ - implementing now in the `geojson` package so users can optionally read and write geobuf format



