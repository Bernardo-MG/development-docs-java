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

## Deprecated Classes in all Maven Submodules

```text
MATCH
   (main:Artifact),
   (pom:Pom)-[:HAS_PARENT]->(main),
   (pom)-[:DESCRIBES]->(submodule:Artifact),
   (jar:Jar)-[:CONTAINS]->(pom),
   (jar:Jar)-[:CONTAINS]->(class:Java:Type),
   (class)-[:ANNOTATED_BY]->(annotation),
   (annotation)-[:OF_TYPE]->(annotationType)
WHERE
   main.name = 'parent-project'
   AND annotationType.fqn = 'java.lang.Deprecated'
RETURN DISTINCT
   class
```

