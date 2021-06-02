# Detecting Problems

## Circular dependencies

```text
MATCH
   (t:Type)-[:DEPENDS_ON*]->(t)
RETURN
   t
```

## Entities used in facade services

```text
MATCH
   (facade:Facade)-[:DECLARES]->(method),
   (method)-[:HAS]->()-[:OF_TYPE*]->(receivedtype:Entity),
   (method)-[:RETURNS]->(returntype:Entity)
WHERE
   (method.visibility="public" OR method.visibility="protected")
RETURN
   facade.name AS service,
   method.name AS method,
   collect(distinct receivedtype.name) AS received,
   returntype.name AS returned
```

## Controllers with public final methods

```text
MATCH (c:Controller)-[:DECLARES]->(m:Method { visibility: 'public' })
WHERE
   EXISTS(m.final)
RETURN
   c.name as controller,
   m.name as method
```

## Default fields

```text
MATCH
   (class)-[:DECLARES]->(field:Field)
WHERE
   field.visibility = 'default'
   AND (
      field.synthetic = false
      OR NOT EXISTS(field.synthetic)
   )
RETURN DISTINCT
   class.name AS class,
   field.name AS field
ORDER BY
   class,
   field
```

## Methods Not Used

```text
MATCH
   (service)-[:DECLARES]->(method:Method)
WHERE
   method.name <> 'null'
   AND NOT ()-[:INVOKES]->(method)
RETURN DISTINCT 
   service.name AS service,
   method.name AS method
```

## Components Not Used

```text
MATCH
   (component:Java:Class)
WHERE
   NOT ()-[:DEPENDS_ON]->(component)
   AND NOT component:Test
   AND NOT component:Controller
   AND NOT component:Configuration
RETURN DISTINCT 
   component.name AS component
```

