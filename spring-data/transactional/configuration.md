# Configuration

## XML

```markup
<beans
   xmlns:tx="http://www.springframework.org/schema/tx"
   xsi:schemaLocation="
      http://www.springframework.org/schema/tx
      http://www.springframework.org/schema/tx/spring-tx.xsd">

   <!-- Activates transactionality -->
   <tx:annotation-driven transaction-manager="transactionManager" />

</beans>
```

## Configuration Class

```java
@Configuration
@EnableTransactionManagement
public class PersistenceConfiguration
```

