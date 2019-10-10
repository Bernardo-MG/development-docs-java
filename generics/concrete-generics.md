# Concrete Generics

It is possible specifying more exactly the type used:

```java
public class WithGeneric<T>;

public class WithGeneric<T extends Number>;
```

It is even possible to define multiple inheritances:

```java
public class WithGeneric<T extends A & B & C>;
```

