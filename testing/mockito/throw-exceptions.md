# Throw Exceptions

```java
Mockito.doThrow(Exception.class).when(service.getEmployee());
```

### Void Methods

```java
Mockito.doThrow(Exception.class).when(service).call();
```

