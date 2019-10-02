# Common Persistence Beans



The persistence context requires the following common beans:

```markup
<!-- Transaction manager -->
<bean id="transactionManager" class="${jpa.transactionManager.class}">
   <property name="entityManagerFactory" ref="entityManagerFactory" />
</bean>

<!-- Entity manager -->
<bean id="entityManager" class="${jpa.entityManager.class}">
   <property name="entityManagerFactory" ref="entityManagerFactory" />
</bean>
```

```text
# Bean classes
jpa.entityManagerFactory.class=org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean
jpa.entityManager.class=org.springframework.orm.jpa.support.SharedEntityManagerBean
jpa.adapter.class=
jpa.transactionManager.class=org.springframework.orm.jpa.JpaTransactionManager

# JPA configuration
jpa.persistenceUnitName=jpa_example
jpa.showSql=false
jpa.packagesToScan=com.bernardomg.example.jpa.model.collection,com.bernardomg.example.jpa.model.converter
```



