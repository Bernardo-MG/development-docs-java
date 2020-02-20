# Wrapping Method

Inside an aspect:

```java
@Aspect
public class ServiceLogger
```

## Before

```java
@Before(value = "execution(* com.bernardomg..*Service*.*(..))",
		argNames = "joinPoint")
public void beforeCall(final JoinPoint joinPoint) {
	LOGGER.debug("Calling {} with arguments {}",
			joinPoint.getSignature().toShortString(), joinPoint.getArgs());
}
```

## After

```java
@AfterReturning(
		value = "execution(* com.bernardomg..*Service*.*(..))",
		returning = "returnValue")
public void afterCall(final JoinPoint joinPoint, final Object returnValue) {
	LOGGER.debug("Called {} and returning {}",
			joinPoint.getSignature().toShortString(), returnValue);
}
```

