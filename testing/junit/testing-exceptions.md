# Testing Exceptions

## JUnit 4

There are two options to test an exception with JUnit 4.

### Annotation

```java
@Test(expected = Exception.class)
public final void testWithException() {
   service.throwsException();
}
```

### Rule

```java
@Rule
public ExpectedException expectedEx = ExpectedException.none();

@Test
public final void testWithException() {
   expectedEx.expect(Exception.class);
   expectedEx.expectMessage("error.message");

   service.throwsException();
}
```

## JUnit 5

### Thrown Exception

```java
@Test
public final void testWithException() {
   Assertions.assertThrows(
      Exception.class,
      service::throwsException);
}
```

### Exception Content

```java
@Test
public final void testWithException() {
   final ExceptionWithCode ex;

   ex = Assertions.assertThrows(ExceptionWithCode .class, service::throwsException);
   
   Assertions.assertEquals(1, ex.getCode());
}
```

