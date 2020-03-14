# Test configuration

## XML

```java
@ContextConfiguration(locations = { "classpath:context/config.xml" })
@TestPropertySource({ "classpath:config/config.properties" })
public class ITSuite {

}
```

## Configuration Classes

```java
@ContextConfiguration(classes = { TestConfiguration.class })
@TestPropertySource({ "classpath:config/config.properties" })
public class ITSuite {

}
```

### Spring Boot

```java
@SpringBootTest(classes = Application.class)
@TestPropertySource({ "classpath:config/config.properties" })
public class ITSuite {

}
```



