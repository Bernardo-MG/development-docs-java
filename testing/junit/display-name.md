# Display Name

JUnit 5 allows defining a descriptive name for tests and suites.

```java
@DisplayName("Example suite")
public class TestSuite {

    @Test
    @DisplayName("Some test")
    public final void test() {
        // Loads tests data
    }

}
```

