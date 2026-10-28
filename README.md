# Cartogrammar map data

Map data used in videos on the Cartogrammar YouTube channel, published as required by the
[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).

## s2-time-zones

Used in the Short "Why Time Zone Maps Make No Sense".

- File: `s2-time-zones/timezones-now-simplified.topojson`
- Source: [timezone-boundary-builder](https://github.com/evansiroky/timezone-boundary-builder) release
  [2026e](https://github.com/evansiroky/timezone-boundary-builder/releases/tag/2026e), asset `timezones-now.geojson.zip` (`combined-now.json`)
- Changes: clipped to latitudes north of 60°S, then simplified. Made with [mapshaper](https://github.com/mbloch/mapshaper) 0.6.121:

```
mapshaper -i combined-now.json -clip bbox=-180,-60,180,90 -simplify interval=500 keep-shapes -o timezones-now-simplified.topojson format=topojson quantization=1000000
```

## License

The data in this repository is a derivative of OpenStreetMap data via timezone-boundary-builder.

© OpenStreetMap contributors. This database is made available under the Open Database License:
https://opendatacommons.org/licenses/odbl/1-0/. Any rights in individual contents of the database are licensed under the
Database Contents License: https://opendatacommons.org/licenses/dbcl/1-0/
