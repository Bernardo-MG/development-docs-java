# Queries

## Custom Queries

Spring can generate queries from the interface methods.

This will create a query for fetching all the entities with a specific name:

```java
public interface EntityRepository extends JpaRepository<Entity, EntityKey> {

   public Iterable<Entity> findByName(final String name);

}
```

## JPQL Queries

It is possible to define the query which a method will use:

```java
@Query("SELECT e FROM Entity e WHERE e.name = :name")
public Iterable<Entity> findByNameJpql(@Param("name") final String name);
```

Notice that it is using a named argument.

### SpEL in Queries <a id="jpa.query.spel-expressions"></a>

To find out automatically the received entity name \(useful when extending the entity\):

```java
@Query("SELECT e FROM #{#entityName} e WHERE e.name = :name")
public Iterable<Entity> findByNameJpql(@Param("name") final String name);
```

