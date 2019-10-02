# Transactional

Transactionality can be marked by using the @Transactional annotation. Note that there is a JPA annotation of the same name, but we are using the Spring one.

## Configuration

This alone won't work, transactionality should be activated through configuration:

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

## Aspects and Final

Transactionality is handled through aspects and the cglib library, which means that transactional classes and methods can't be final.



