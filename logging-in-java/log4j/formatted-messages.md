# Formatted Messages

These can be formatted with the use of Java's formatter:

```java
Logger logger = LogManager.getFormatterLogger("Foo");

logger.debug("Logging in user %s", user.getName());
```

