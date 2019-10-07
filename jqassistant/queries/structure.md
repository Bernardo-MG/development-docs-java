# Structure

## Types extending a base type, along the base type

```text
MATCH
   (component:Type {name: 'ClassName'}),
   (extension:Type)-[:EXTENDS|IMPLEMENTS*0..]->(component)
RETURN
   extension
```

## Methods, including inherited methods, of a class

```text
MATCH
   (component:Type {name: 'CrudService'}),
   (component)-[:EXTENDS|IMPLEMENTS*0..]->()-[:DECLARES]->(inheritedMethod:Method)
RETURN
   component,
   inheritedMethod
```

## Methods annotated with PreAuthorize and the permission used

```text
MATCH
   (service:Type)-[:DECLARES]->(method:Method),
   (method:Method)-[:ANNOTATED_BY]->(annotation:Annotation)-[:OF_TYPE]->(annotationType:Type),
   (annotation:Annotation)-[:HAS]->(annotationValue:Value{ name:'value' })
WHERE
   annotationType.fqn = 'org.springframework.security.access.prepost.PreAuthorize'
RETURN
   service.name AS service,
   method.name AS method,
   extract(p in apoc.text.regexGroups(annotationValue.value, "\\('([a-zA-Z]*)', '[crud]'\\)") | p[1]) as permission
```

## Methods In a Maven Module

```text
MATCH
   (artifact:Artifact {name :'module-name'}),
   (artifact)-[:CONTAINS*..]->(class:Class)
RETURN
   artifact.name AS artifact,
   class.name AS class
```

