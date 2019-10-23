# Asking for a Specific Bean

```java
public class ExampleService implements Service {

   @Autowired
   @Qualifier("dependencyB")
   private Component dependency;

}
```

