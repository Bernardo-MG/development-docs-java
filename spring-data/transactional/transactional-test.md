# Transactional Test

To create a transactional test with JUnit 5:

```java
@RunWith(JUnitPlatform.class)
@SpringJUnitConfig
@Transactional
@Rollback
public class TransactionalTest
```

