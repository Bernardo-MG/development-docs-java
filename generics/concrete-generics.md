# Bounded Parameters

It is possible specifying more exactly the type used:

```java
public class WithGeneric<T>;

public class WithGeneric<T extends Number>;
```

## Multiple Bounds

```java
public class WithGeneric<T extends A & B & C>;
```

