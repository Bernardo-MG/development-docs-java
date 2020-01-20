# Verify Calls

## Called once, and only once

```java
Mockito.verify(service, Mockito.times(1)).method(ArgumentMatchers.any());
```

## Called one or more times

```java
Mockito.verify(service, Mockito.atLeastOnce()).method(ArgumentMatchers.any());
```

## Never Called

```java
Mockito.verify(service, Mockito.never()).method(ArgumentMatchers.any());
```

## Called with a specific value

```java
Mockito.verify(response, Mockito.atLeastOnce()).setContentType(
   ArgumentMatchers.same(MediaType.APPLICATION_PDF_VALUE));
```



