# Initialization

## Annotations

```java
public class Bean {

   @PostConstruct
   public void initialize() {
      // Code
   }

}
```

## Interface

```java
public class Bean implements InitializingBean {

   @Override
   public void afterPropertiesSet() throws Exception {
      // Code
   }

}
```

