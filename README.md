# neo4j-browser-images

![neo4j-browser-images](https://user-images.githubusercontent.com/5991751/28341303-e967c7c0-6bc7-11e7-8f05-8aaaa9c97cca.png)



A d3 hack to allow the Neo4j Browser to render images in nodes.

Special thanks to Michael Hunger.


## Images

Create node property called `image_url` and populate this with a fully qualified image url.


```
MATCH (n:MyImageNode)
SET n.image_url = "http://myimage.png"
RETURN n
```

smaller images (100x100 px) work better, use the largest node size (80px) for best effect.

## Run in Neo4j Desktop

Update Neo4j Desktop, copy and paste the npm repo link (below) in the 'Install Graph Application' box, and then add Neo4j Browser Images app to your Project.

https://registry.npmjs.org/neo4j-browser-image-enabled

<img width="299" alt="graph-app-url" src="https://user-images.githubusercontent.com/5991751/50950037-878a1b80-145d-11e9-900e-4949b78af427.png">

## Run Standalone

Works best with smaller (100x100 px) square images.

#### 1. clone
 [neo4j-browser](https://github.com/neo4j/neo4j-browser), follow the yarn build instructions.

#### 2. copy

***current version***

Copy init.js to this location, replacing the original.

/neo4j-browser/src/browser/modules/D3Visualization/lib/visualization/renders/init.js

***older versions (< commit \#846)***

Copy init.coffee to this location, replacing the original.

/neo4j-browser/src/browser/modules/D3Visualization/lib/visualization/renders/init.coffee

#### 3. launch

`$ yarn start`

 Open http://localhost:8080 in your browser.

Connect to Neo4j using `localhost` and your credentials.
