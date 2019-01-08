# neo4j-browser-images

![neo4j-browser-images](https://user-images.githubusercontent.com/5991751/28341303-e967c7c0-6bc7-11e7-8f05-8aaaa9c97cca.png)



A d3 hack to allow the Neo4j Browser to render images in nodes.

Works best with smaller (100x100 px) square images.

#### 1. clone neo4j-browser
 [neo4j-browser](https://github.com/neo4j/neo4j-browser), follow the yarn build instructions.

#### 2. copy this file

***current version***

Copy init.js to this location, replacing the original.

/neo4j-browser/src/browser/modules/D3Visualization/lib/visualization/renders/init.js

***older versions (< commit 846)***

Copy init.coffee to this location, replacing the original.

/neo4j-browser/src/browser/modules/D3Visualization/lib/visualization/renders/init.coffee

####3. launch neo4-browser

`$ yarn start`

 Open http://localhost:8080 in your browser.

Connect to Neo4j using `localhost` and your credentials.

Set a property named image_url with a fully qualified url

```
MATCH (n:MyImageNode)
SET n.image_url = "http://myimage.png"
RETURN n
```
The node will now render with your image.

Use the max node size (80px) for best effect.

Special thanks to Michael Hunger.
