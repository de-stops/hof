# hof-stops

This is a simple script to download [Landkreis Hof](http://www.landkreis-hof.de/Wirtschaft-Verkehr/Verkehr.aspx) and [Stadt Hof](http://www.stadt-hof.de/hof/hof_deu/leben/oeff-nahverkehr-01.html) stops as [GTFS-compatible CSV](https://developers.google.com/transit/gtfs/reference/stops-file).

The script uses the following endpoint:

```
http://www.bayern-fahrplan.de/XML_COORD_REQUEST?&jsonp=&boundingBox=&boundingBoxLU={minx}%3A{miny}%3AWGS84%5BDD.DDDDD%5D&boundingBoxRL={maxx}%3A{maxy}%3AWGS84%5BDD.DDDDD%5D&coordOutputFormat=WGS84%5BGGZHTXX%5D&type_1=STOP&outputFormat=json&inclFilter=1
```

It starts from bounding box `(11.4, 50, 12.3, 50.5)` and works down to smaller quadrants.

The script produces CSV output in the following format:

```
"stop_id","stop_name","stop_lon","stop_lat","stop_code"
"3400040","Hof (Saale), Umspannwerk",11.9386536871,50.319623910800004,"de:9464:40"
```

# Usage

```
npm install
npm run export
```

# Disclaimer

Usage of this script may or may not be legal, use on your own risk.  
This repository provides only source code, no data.

# License

Source code is licensed under [BSD 2-clause license](LICENSE). No license and no guarantees implied on the produced data, produce and use on your own risk.