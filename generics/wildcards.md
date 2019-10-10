# Wildcards

If needed a wildcard generic type, which accepts any type, can be used:

```java
public void function(List<?> list);
```

```java
function(new ArrayList<String>());

function(new ArrayList<Double>());
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

