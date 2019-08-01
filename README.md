# OpenStreetMap Carto Italian

![screenshot](https://raw.github.com/ammatwain/openstreetmap-carto-italian/master/preview.png)

These are the CartoCSS map stylesheets for the Standard map layer on [OpenStreetMap.org](https://www.openstreetmap.org/#map=9/33.9229/35.8772).

This version has been modified to represent geographic names giving priority to the following languages:
1) Italian
2) English
3) French
3) Local language (relative to the map)

# Installation

You need a PostGIS database populated with OpenStreetMap data along with auxillary shapefiles.
See [INSTALL.md](INSTALL.md).

# Database Import (with osm2pgsql)
<pre>
osm2pgsql -d gis \
  --create --slim -G \
  --hstore-all \
  --tag-transform-script /your/path/openstreetmap-carto-italian/openstreetmap-carto-italian.lua \
  -C 2500 \
  --number-processes 1 \
  -S /your/path/openstreetmap-carto-italian/openstreetmap-carto-italian.style \
  /your/path/lebanon-latest.osm.pbf
</pre>

# Roadmap

## First Commit ( 2019-07-31)

This was a full re-implementation of the original OpenStreetMap Carto style,

( see  [openstreetmap-carto](https://github.com/gravitystorm/openstreetmap-carto) )

# Alternatives

There are many open-source stylesheets written for creating OpenStreetMap-based
maps using Mapnik, many based on this project. Some alternatives are:

* [openstreetmap-carto](https://github.com/gravitystorm/openstreetmap-carto)
* [OSM-Bright](https://github.com/mapbox/osm-bright)
* [XML-based stylesheets](https://trac.openstreetmap.org/browser/subversion/applications/rendering/mapnik)
* [osmfr-cartocss](https://github.com/cquest/osmfr-cartocss)
* [openstreetmap-carto-german](https://github.com/giggls/openstreetmap-carto-de)

# Maintainers
(for this version)

* Amedeo Sorpreso [@ammatwain](https://github.com/ammatwain/)

(for original version)

( see  [openstreetmap-carto](https://github.com/gravitystorm/openstreetmap-carto) )
