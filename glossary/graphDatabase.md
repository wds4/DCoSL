graph database
======

A graph database, as opposed to a relational database, stores data using nodes and relationships instead of tables or documents.

Although graph databases are not required for the DCoSL protocol, especially in the early stages, they are particularly well suited for DCoSL, particularly at later stages and with large, sprawling [concept graphs](conceptGraph.md). Open source graph databases such as [neo4j](https://github.com/neo4j/neo4j) are generally accompanied by a graph query language, such as neo4j's [cypher](https://neo4j.com/docs/getting-started/cypher-intro/)). 

To search for all [class threads](classThread.md) within a concept graph, use the cypher query:

```
MATCH p = (a)-[r1]->(b)-[r2]->(c)-[r3 *0..5]-(d)-[r4]->(e)

WHERE a.wordTypes.includes('jsonSchema')
AND b.wordType = 'wordType'
AND c.wordType = 'superset'
AND d.wordType = 'set'

AND r1.type = 'isTheJsonSchemaFor'
AND r3.type = 'subsetOf'
AND r4.type = 'specificInstanceOf'
RETURN nodes(p)
```

(NOTE: It's been long time since I've written cypher queries; likely multiple syntax errors in the above; will need to fix)

The equivalent query in a relational database would require multiple joins and would be much less efficient.

Various definitions of a graph database:
- [wikipedia](https://en.wikipedia.org/wiki/Graph_database)
- [neo4j](https://neo4j.com/docs/getting-started/get-started-with-neo4j/graph-database/)
- [oracle](https://www.oracle.com/autonomous-database/what-is-graph-database/)
