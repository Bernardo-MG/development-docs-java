# Bound Parameters

It is possible specifying more exactly the type used:

```java
public class WithGeneric<T>;

public class WithGenericNumber<T extends Number>;
```

```java
// Valid
new WithGeneric<String>();

// Compile error
new WithGenericNumber<String>();
```

## Multiple Bounds

```java
public class WithGeneric<T extends A & B & C>;
```

