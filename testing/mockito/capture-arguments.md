# Capture Arguments

```java
final ArgumentCaptor<Short> captor;
final Short captured;

captor = ArgumentCaptor.forClass(Short.class);

// Mocked service
service.someMethod(arg1, arg2);

Mockito.verify(service, Mockito.atLeastOnce()).someMethod(ArgumentMatchers.any(), captor.capture());

// The value 
captured = captor.getValue();
```

