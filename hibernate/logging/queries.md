# Queries

## Log4j Configuration

```markup
<Logger name="org.hibernate.SQL" level="debug" additivity="false">
   <AppenderRef ref="console" />
</Logger>

<Logger name="org.hibernate.type.descriptor.sql" level="trace" additivity="false">
   <AppenderRef ref="console" />
</Logger>
```



