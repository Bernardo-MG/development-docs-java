# Persistence

## Sequences Defined in Entities

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

## Tables Mapped by Entities

```text
MATCH
   (entity:Entity),
   (entity)-[:ANNOTATED_BY]->(annotation:Annotation),
   (annotation)-[:OF_TYPE]->(annoType),
   (annotation)-[:HAS]->(attribute)
WHERE
   annoType.name = 'Table'
   AND attribute.name = 'name'
RETURN
   attribute.value AS table
ORDER BY
   table
```

