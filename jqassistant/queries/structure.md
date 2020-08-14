# Structure

## Types extending a base type, along the base type

```text
MATCH
   (class),
   (extension:Type)-[:EXTENDS|IMPLEMENTS*0..]->(class)
WHERE
   class.name = 'ClassName'
RETURN
   extension
```

## Methods, including inherited methods, of a class

```text
MATCH
   (class),
   (class)-[:EXTENDS|IMPLEMENTS*0..]->()-[:DECLARES]->(inheritedMethod:Method)
WHERE
   class.name = 'ClassName'
RETURN
   class.name AS class,
   inheritedMethod AS method
```

## Classes and methods data

```text
MATCH
   (class:Type),
   (class)-[:DECLARES]->(method:Method),
   (package:Package)-[:CONTAINS]->(class)
RETURN DISTINCT
   package.fileName AS package,
   class.name AS class,
   class.fileName AS fileName,
   class.fqn AS fullyQualifiedName,
   class.sourceFileName AS sourceFileName,
   class.javaVersion AS javaVersion,
   class.md5 AS md5,
   method.name AS method,
   method.signature AS methodSignature,
   method.firstLineNumber AS firstLine,
   method.lastLineNumber AS lastLine,
   method.effectiveLineCount AS lines,
   method.cyclomaticComplexity AS cyclomaticComplexity,
   class.valid AS validClass,
   class.visibility AS classVisibility,
   method.visibility AS methodVisibility
ORDER BY
   package,
   class,
   method
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

##  Methods Nobody Calls

```text
MATCH
   (class:Type)-[:DECLARES]->(method:Method)
WHERE
   NOT ()-[:INVOKES]->(method)
RETURN
   class,
   method
```

## Non-public methods with annotations

```text
MATCH
   (component:Type)-[:DECLARES]->(method:Method),
   (method:Method)-[:ANNOTATED_BY]->(annotation:Annotation)-[:OF_TYPE]->(annotationType:Type)
WHERE
   method.visibility IN ['private', 'protected']
   AND NOT annotationType.fqn = 'java.lang.Deprecated'
RETURN DISTINCT
   component.name AS component,
   method.name AS method,
   annotationType.name AS annotation
```

