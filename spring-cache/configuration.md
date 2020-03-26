# Configuration

## Method Configuration

```java
@Cacheable("employees")
public Iterable<N> readEmployees(final Short code, final Short company, final Pageable pageable);
```

## Custom Key

```java
@Cacheable(cacheNames = "employees", key = "{ #root.methodName, #code, #company }")
public Iterable<N> readEmployees(final Short code, final Short company, final Pageable pageable);
```

## Registration

Any named cache should be registered, for example in an ehcache configuration file.

