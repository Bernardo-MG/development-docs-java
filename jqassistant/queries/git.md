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

## git History

```text
MATCH
   (commit:Git:Commit),
   (commit)-[:CONTAINS_CHANGE]->(change:Git:Change),
   (author:Git:Author)-[:COMMITTED]->(commit),
   (change)-[]->(file:File)
RETURN DISTINCT
   commit.sha AS sha,
   commit.date AS date,
   commit.time AS time,
   commit.author AS author,
   author.email AS author_email,
   author.identString AS author_id,
   commit.committer AS commiter,
   commit.message AS message,
   change.modificationKind AS modificationKind,
   file.fileName AS file
```

