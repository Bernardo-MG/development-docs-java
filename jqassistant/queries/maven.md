# Maven

## Submodules

```text
MATCH
   (main:Artifact),
   (pom:Pom)-[:HAS_PARENT]->(main),
   (pom)-[:DESCRIBES]->(submodule:Artifact)
WHERE
   main.name = 'parent-project'
RETURN DISTINCT
   main.name AS main,
   submodule.name AS submodule,
   pom.name AS name
ORDER BY
   main,
   submodule
```

## Declared dependencies

```text
MATCH
   (project:Pom),
   (project)-[:DECLARES_DEPENDENCY]->()-[:TO_ARTIFACT]->(dependency)
WHERE
   project.artifactId= 'project-name'
RETURN DISTINCT
   project.name AS project,
   dependency.name AS dependency
ORDER BY
   project,
   dependency
```

## Declared dependencies on all submodules

```text
MATCH
   (main:Artifact),
   (pom:Pom)-[:HAS_PARENT]->(main),
   (pom)-[:DESCRIBES]->(submodule:Artifact),
   (pom)-[:DECLARES_DEPENDENCY]->()-[:TO_ARTIFACT]->(dependency)
WHERE
   main.name = 'parent-project'
RETURN DISTINCT
   submodule.name AS submodule,
   dependency.name AS dependency
ORDER BY
   submodule,
   dependency
```

## Classes in a project

```text
MATCH
   (pom:Pom),
   (jar:Jar)-[:CONTAINS]->(pom),
   (jar:Jar)-[:CONTAINS]->(class:Java)
WHERE
   pom.artifactId = 'project-name'
   AND ((class:Class) OR (class:Interface))
RETURN DISTINCT
   class.name AS class
ORDER BY
   class
```

## Classes in all submodules

```text
MATCH
   (main:Artifact),
   (pom:Pom)-[:HAS_PARENT]->(main),
   (pom)-[:DESCRIBES]->(submodule:Artifact),
   (jar:Jar)-[:CONTAINS]->(pom),
   (jar:Jar)-[:CONTAINS]->(class:Java)
WHERE
   main.name = 'parent-project'
   AND ((class:Class) OR (class:Interface))
RETURN DISTINCT
   class.name AS class
ORDER BY
   class
```

## Number of internal module dependencies

```text
MATCH
   (main:Maven:Main)-[r:DEPENDS_ON]->(dependency:Maven:Main)
RETURN
   main.name AS module,
   COUNT(r) AS dependenciesCount,
   COLLECT(dependency.name) AS dependencies
ORDER BY
   dependenciesCount DESC,
   module
```

