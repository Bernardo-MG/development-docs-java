# Maven

## Submodules

```text
MATCH
   (main:Artifact{name: 'parent-project'}),
   (pom:Pom)-[:HAS_PARENT]->(main),
   (pom)-[:DESCRIBES]->(submodule:Artifact)
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
   (project:Pom{artifactId: 'project-name'}),
   (project)-[:DECLARES_DEPENDENCY]->()-[:TO_ARTIFACT]->(dependency)
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
   (main:Artifact{name: 'parent-project'}),
   (pom:Pom)-[:HAS_PARENT]->(main),
   (pom)-[:DESCRIBES]->(submodule:Artifact),
   (pom)-[:DECLARES_DEPENDENCY]->()-[:TO_ARTIFACT]->(dependency)
RETURN DISTINCT
   submodule.name AS submodule,
   dependency.name AS dependency
ORDER BY
   submodule,
   dependency
```

## All  the Classes in a Module

```text
MATCH
   (main:Artifact),
   (child)-[:HAS_PARENT]->(main),
   (child)-[:DESCRIBES]->(directory:Artifact:Directory),
   (directory)-[:CONTAINS]->(class:Type)
WHERE
   main.name = 'parent-module-name'
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

