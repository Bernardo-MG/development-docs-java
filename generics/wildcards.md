# Wildcards

If needed a wildcard generic type, which accepts any type, can be used:

```java
List<?> list;
```

## Bounds

This is an upper bounds wildcard:

```java
List<? extends Number> list;
```

Which accepts Number and it subclasses.

This is an lower bounds wildcard:

```java
List<? super Number> list;
```

Which accepts Number and it super-classes.

