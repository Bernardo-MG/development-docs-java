# File Structure

## Jar containing a class

```text
MATCH
   (class:Java),
   (jar:Jar)-[:CONTAINS]->(class)
WHERE
   class.name = 'classname'
RETURN DISTINCT
   jar.fileName AS jar,
   class.name AS name
```

