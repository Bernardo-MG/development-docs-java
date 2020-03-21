# Transaction Aspect

## XML

```markup
<tx:advice id="transactionAdvice" transaction-manager="transactionManager">
  <!-- the transactional semantics... -->
  <tx:attributes>
	 <!-- all methods starting with 'get' are read-only -->
	 <tx:method name="get*" read-only="true" />
	 <!-- other methods use the default transaction settings (see below) -->
	 <tx:method name="*" />
  </tx:attributes>
</tx:advice>

<!-- ensure that the above transactional advice runs for any execution 
  of an operation defined by the FooService interface -->
<aop:config>
  <aop:pointcut id="serviceOperation"
	 expression="execution(* com.company..*Service*.*(..))" />
  <aop:advisor advice-ref="transactionAdvice"
	 pointcut-ref="serviceOperation" />
</aop:config>
```

