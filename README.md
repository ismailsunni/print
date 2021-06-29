

## Data

### Creating a test MVT dataset

- Draw a GPX
- Convert it to GeoJSON: ogr2ogr output.geojson input.gpx tracks
- Create vector tiles:
  - git clone https://github.com/mapbox/tippecanoe.git
  - cd tippecanoe ; make -j; cd -
  - tippecanoe/tippecanoe output.geojson -e public/tiles --no-tile-compression
