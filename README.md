# neo4j-browser-images

A d3 hack to allow the Neo4j Browser to render images in nodes.

Works best with square images.

Clone neo4j-browser, follow the yarn build instructions.

Copy init.coffee to this location, replacing the original.

/neo4j-browser/src/browser/modules/D3Visualization/lib/visualization/renders/init.coffee

Restart yarn. Open http://localhost:8080 in your browser.

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
