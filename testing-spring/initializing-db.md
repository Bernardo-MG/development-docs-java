# Initializing DB

The SQL annotation will load the specified scripts.

It can be applied at the class level.

```java
@Sql({ "/testconf/db/initialData.sql" })
public class Test
```

Or at the method. In this case it will override the configuration set for the class.

```java
@Sql({ "/testconf/db/additionalData.sql" })
public void testMethod()
```

