# Mapped Diagnostic Context

The MDC allows using custom variables in the log:

```text
%-5p | %X{principal}
```

In this case the "principal" variable is loaded through the MDC, as the "X" command tells.

This requires that same variable to be registered:

```java
MDC.put("principal", context.getAuthentication().getName());
```

