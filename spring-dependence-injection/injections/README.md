# Injections

## Field

```java
public class ExampleService implements Service {

   @Autowired
   private Component dependency;

}
```

## Constructor

```java
public class ExampleService implements Service {

   private final Component dependency;

   @Autowired   
   public ExampleService(final Component component) {
      super();

      dependency = component;
   }

}
```

## Setter

```java
public class ExampleService implements Service {

   private Component dependency;

   @Autowired
   public void setDependency(final Component component) {
      dependency = component;
   }

}
```

