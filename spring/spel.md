---
description: Spring Expression Language
---

# SpEL

## Operations

### Acquiring a Bean

Using the name of a value or a constant:

```text
#{beanName}
```

```text
#{property.name}
```

Properties can be used:

```text
#{${property.name}}
```

Or a reference to a registered bean:

```text
#{@beanName}
```

It is possible to get a factory:

```text
#{&beanName}
```

### Checking Properties

```text
#{'${property.name}'.contains('Some text')}
```

### Default Values

```text
${properties.booleanValue:false}
```

It may be the empty string:

```text
${properties.textValue:}
```

### Type Safe Operations

```text
#{bean?.field}
```

## More Information

* [Spring Expression Language](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#expressions)

