# Bozeman building permit

Data log for building permit

Data from
https://data.datamontana.us/City-of-Bozeman/Bozeman-Building-Permits-4-11-96-to-4-15-14/rxsc-ky44

Location column split to lat/long columns using Google sheets
https://docs.google.com/spreadsheets/d/1HlbSAvzWikiZfuZQIVBnUDUJ-X6B-15Bno72E3Ixwd4/edit#gid=1443128770

Added key column, renamed other columns to remove spaces, be lowercase

Downloaded as csv

Converted from .csv to geojson using csvkit
Documentation used:
http://csvkit.readthedocs.org/en/latest/scripts/csvjson.html
Terminal command used:
csvjson --lat lat --lon long --k key -i 4 bzn-building-permit-data.csv > bzn-permit.geojson

Added "bznPermits = " to beginning of geoJson file (there has to be a better way to do this?)

Coded Leaflet.js map in bzn-dev-map.html to display points
Reference tutorial
http://leafletjs.com/examples/geojson.html