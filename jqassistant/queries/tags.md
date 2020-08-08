# Tags

## Deprecated Classes

```text
MATCH
   (class)-[:ANNOTATED_BY]->(annotation),
   (annotation)-[:OF_TYPE]->(annotationType)
WHERE
   annotationType.fqn = 'java.lang.Deprecated'
RETURN DISTINCT
   class
```

