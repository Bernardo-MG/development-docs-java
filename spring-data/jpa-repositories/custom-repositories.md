# Custom Repositories

Repositores can be extended with custom code. This requires the following classes:

* Spring repository interface
* Custom repository interface
* Custom repository implementation

```java
public interface EntityCustomRepository  {

   public Iterable<Entity> findByCustomQuery();

}
```

```java
public interface EntityRepository extends JpaRepository<Entity, EntityKey> extends EntityCustomRepository {

}
```

```java
public class EntityCustomRepositoryImpl implements EntityCustomRepository   {

   public final Iterable<Entity> findByCustomQuery() {
      // Implementation
   }

}
```

Now calling the findByCustomQuery method in the repository will call the method in theDefautlEntityCustomRepository implementation. Spring will mix this code with the repository it generates.

```java
public final class EntityService {

   @Autowired
   private EntityRepository repository;

   public final Iterable<Entity> getByCustomQuery(){
      return repository.findByCustomQuery();
   }

}
```

