# Configuration

## Method Configuration

```java
@Cacheable(cacheNames = "employees")
public Iterable<N> readEmployees(final Short code, final Short company, final Pageable pageable);
```

## Registration

Any named cache should be registered, for example in an ehcache configuration file.

