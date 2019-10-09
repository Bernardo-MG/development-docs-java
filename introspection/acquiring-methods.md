# Properties

```java
final Collection<PropertyDescriptor> descs;

descs = Arrays.asList(Introspector.getBeanInfo(object.getClass()).getPropertyDescriptors());
```

## Is It a Getter?

```java
final Boolean getter;

getter = (pd.getReadMethod() != null);
```

## Is It Annotated?

```java
final Boolean annotated;

annotated= pd.getReadMethod().getAnnotation(Column.class);
```

## Invoking a Getter

This will return the property value:

```java
final PropertyDescriptor pd;
final Object value;

pd = Iterables.getFirst(descs, null);

value = pd.getReadMethod().invoke(object);
```

