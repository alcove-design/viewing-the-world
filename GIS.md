## How to integrate Stamen map tiles to blender using blenderGIS


Quick and dirty way:

Edit the servicesDefs.py (located at `~/.config/blender/{versionNum}/scripts/addons/blenderGIS-225/core/basemaps`)


Add the following entry to the list of sources:


```
	"STAMEN" : {
		"name" : 'Stamen',
		"description" : 'Stamen OSM',
		"service": 'TMS',
		"grid": 'WM',
		"quadTree": False,
		"layers" : {
			"STAMEN" : {"urlKey" : '', "name" : 'Stamen', "description" : '', "format" : 'jpeg', "zmin" : 0, "zmax" : 19}
		},
		"urlTemplate": "http://tile.stamen.com/watercolor/{Z}/{X}/{Y}.jpg",
		"referer": ""
	},
```

Restart blender, voilà.

Todo: open an issue and eventually submit a pull request
