Q1: What is the URL of the WMS GetCapabilities request?
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

Q2: What is the URL of the WFS GetCapabilities request?
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities

Q3: Submit a screenshot of your updated WFS Layer Preview
![Q3](<WFS Layer Preview.png>)

Q4: What does drawing order refer to? Which layer goes on top, the first or the last layer in the list? Dem drawing orders refers to the sequence in which the layers are rendered on a map.  The layer that goes on top is the layer higher on the list and the layers lower in the list are drawn last.

Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.
![Q5](<Layer Preview of SF Layer Group.png>)

Q6: What is the WMS url for the single-tiled request?
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=1901&HEIGHT=1000&BBOX=592892.9538703056%2C4915879.267359864%2C601959.6898544787%2C4920651.233667323

Q7: What is the WMS url for one of the tiled requests? What is the image size?
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG%3A26713&BBOX=596152.2068582997%2C4918255.70658098%2C597373.8302330093%2C4919477.32995569. 

Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url? Tile level is 13 and TileRow is 2037. This URL requests a map tile from the "spearfish" layer, using the EPSG:4326 coordinate system, at zoom level 13, with a tile located at column 3468 and row 2073, in PNG format.
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A13&TileCol=3468&TileRow=2073 

Q9: In the zoomed-out URL, what are the TileCol and TileRow? TileCol=3465 and TileRow=2074
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A13&TileCol=3465&TileRow=2074

Q10: In the zoomed-in URL, what are the TileCol and TileRow? TileCol=6932 and TileRow=4150
https://scaling-adventure-9gqjr6rgxwvfp4g5-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A14&TileCol=6932&TileRow=4150

Q11: Why are they so different for the same location in the map? The TileCol and TileRow values are different even though its in the same location because at higher zoom levels, the map is divided into more smaller tiles. When you zoom in, that area on the map will take up more tiles and the number is bigger.

Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, :.What does the number after EPSG:4326 mean? The TileMatrix refers to a specific zoom  level in the WMTS. The number after EPSG:4326 inicates the zoom level of the map tiles and a higher number means the map is zoomed in more.  Which means smaller tiels represent a smaller area. 