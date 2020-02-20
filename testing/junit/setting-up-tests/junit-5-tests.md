# JUnit 5 Tests

The newer version need a runnable class, marked with @Test and a runner.

Some annotations may be named the same, but they come from other packages.

Most importantly, the assertions now come from a different class.

```java
@DisplayName("A test suite")
public class TestSuite {

    @Test
    public final void alwaysTrue() {
        Assertions.assertTrue(true);
    }

}
```

## Compatibility with Junit 4

With the JUnitPlatform runner allows old IDEs to interpret JUnit 5 tests.

```java
@RunWith(JUnitPlatform.class)
@DisplayName("A test suite")
public class TestSuite {

    @Test
    public final void alwaysTrue() {
        Assertions.assertTrue(true);
    }

}
```

## Integration Test

```java
@SpringJUnitConfig
@ContextConfiguration(classes = { TestConfig.class })
@TestPropertySource({ "classpath:config/test.properties" })
@DisplayName("An integration test suite")
public class ITSuite
```

