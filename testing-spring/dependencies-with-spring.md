# Setting Up Junit

## Unit Test

```java
@RunWith(JUnitPlatform.class)
public class TestSuite {

    @Test
    public final void someTest() {
        // Testing code inside
    }

}
```

## Integration Test

```java
@RunWith(JUnitPlatform.class)
@SpringJUnitConfig
@ContextConfiguration(locations = { "classpath:context/config.xml" })
@TestPropertySource({ "classpath:config/config.properties" })
public class ITSuite {

    @Test
    public final void someTest() {
        // Testing code inside
    }

}
```

