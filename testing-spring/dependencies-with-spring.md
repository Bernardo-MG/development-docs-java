# Setting Up Junit

Spring will need a bit of additional configuration to allow injecting dependencies.

```java
@RunWith(JUnitPlatform.class)
@SpringJUnitConfig
@ContextConfiguration(locations = { "classpath:context/config.xml" })
@TestPropertySource({ "classpath:config/config.properties" })
public class TestSuite {

    @Test
    public final void someTest() {
        // Testing code inside
    }

}
```

