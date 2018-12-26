# Gremlin with Neo4j

An experiment using Gremlin with Neo4j graph database.

## Using

For use the project, simple run this commands:

``` bash
# starting neo4j database and the gremlin server
docker-compose up -d

# running gremlin console
docker-compose run --rm gremlin-console

# connecting to the neo4j instance
:remote connect tinkerpop.server conf/remote-docker-compose.yml
:remote console

# now you can start creating the graphs
graph = Neo4jGraph.open("/data/graph.db/")
g = graph.traversal()
g.V().count()
```

## References

Configuration based in [this repository](https://github.com/gremlin-orm/gremlin-orm-neo4j) of [Gremlin ORM](https://github.com/gremlin-orm/gremlin-orm). Thanks!
