# Resolving Sort and Pageable Arguments

By using an argument resolvers pagination data can be generated from a request:

```java
@GetMapping(produces = MediaType.APPLICATION_JSON_UTF8_VALUE)
public final Iterable<ModelObject>
            getObjects(final Pageable page) {
    return getBusinessService().getObjects(page);
}
```

## XML Configuration

First define the resolvers:

```markup
<bean id="sortResolver" class="resolver.sort.class=org.springframework.data.web.SortHandlerMethodArgumentResolver" />
<bean id="pagingResolver" class="resolver.pageable.class=org.springframework.data.web.PageableHandlerMethodArgumentResolver">
   <constructor-arg ref="sortResolver" />
</bean>
```

Then register them:

```markup
<mvc:annotation-driven>
   <mvc:argument-resolvers>
      <ref bean="sortResolver" />
      <ref bean="pagingResolver" />
   </mvc:argument-resolvers>
</mvc:annotation-driven>
```

