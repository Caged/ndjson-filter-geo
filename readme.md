A hack on top of https://github.com/mbostock/ndjson-cli which filters features based on geometry intersections. Much of this lifted from the existing [ndjson-filter](https://github.com/mbostock/ndjson-cli/blob/master/ndjson-filter) implementation. 

``` bash
cat test/grid.json \
  | ./ndjson-filter-geo --feature <(cat test/oregon.json) 'intersects(d)' \
  | ndjson-filter 'd.properties.UL_LAT > 46'
```
