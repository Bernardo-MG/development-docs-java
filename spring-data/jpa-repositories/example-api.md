# Example API

Spring Data includes an API for querying through samples:

```java
Example<Employee> example;
Iterable<Employee> employees;

example = Example.of(emp);

employees = repository.findAll(example);
```

