# Sorting and Paging

If a method receives a Sort or Pageable parameter it will be applied to the query.

This works with custom queries:

```java
public Page<Employee> findByName(final String name, final Pageable page);

public List<Employee> findByName(final String name, final Sort sort);
```

