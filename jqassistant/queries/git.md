# git

## Number of Times each File has Changed

```text
MATCH
   (change:Git:Change),
   (change)-[]->(file:File)
RETURN DISTINCT
   file.fileName AS file,
   count(change) AS changes
```

