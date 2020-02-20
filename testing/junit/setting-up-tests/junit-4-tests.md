# JUnit 4 Tests

```java
public class TestSuite {

    @Test
    public final void alwaysTrue() {
        Assert.assertTrue(true);
    }

}
```

## Integration Test With Spring

```java
@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration(classes = { TestConfig.class })
@TestPropertySource({ "classpath:config/test.properties" })
@DisplayName("An integration test suite")
public class ITSuite
```

