# neo4j-browser-images

A d3 hack to allow Neo4j Browser to render images in nodes.

Works best with square images.

Clone neo4j-browser, follow the yarn build instructions

replace the init.coffee located here

/neo4j-browser/src/browser/modules/D3Visualization/lib/visualization/renders/init.coffee

Restart yarn

Set a property named image_url with a fully qualified url

```
MATCH (n:MyImageNode)
SET n.image_url = "http://myimage.png"
RETURN n
```
The node will now render with your image.

Use the max node size (80px) for best effect.
