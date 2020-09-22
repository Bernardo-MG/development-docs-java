# Persistence

## All the Sequences Defined in Entities

```text
MATCH
   (entity:Entity),
   (entity)-[:DECLARES]->(method:Method),
   (method)-[:ANNOTATED_BY]->(annotation:Annotation),
   (annotation)-[:OF_TYPE]->(annoType),
   (annotation)-[:HAS]->(attribute)
WHERE
   annoType.name = 'SequenceGenerator'
   AND attribute.name = 'sequenceName'
RETURN
   attribute.value AS sequence
ORDER BY
   sequence
```

