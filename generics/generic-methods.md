# Generic Methods

This can be applied to methods:

```java
public <V> V process(final V input);
```

This example will force the input and output to be the same type.

```java
ModelObject input;
ModelObject output:

input = new ModelObject();
output= new ModelObject();

output = process(input);
```

