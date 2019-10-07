# Repositories

Spring offers a Repository interface for implementing the repository pattern.

In most cases these repositories will work without the need of a concrete implementation, Spring will generate the final repository from the interface.

```java
public interface EntityRepository extends JpaRepository<Entity, EntityKey> {

}
```

In this case the interface used is an extension specific for JPA.

## Bae Repositories

```java
@NoRepositoryBean
public interface BaseRepository extends JpaRepository<Entity, EntityKey>
```

## More Information

* [Working with Spring Data Repositories](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#repositories)

