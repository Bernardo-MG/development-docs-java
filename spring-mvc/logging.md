# Logging

## Logging Requests

```java
@Bean
public CommonsRequestLoggingFilter controllerRequestLogger()
{
   final CommonsRequestLoggingFilter filter;

   filter = new CommonsRequestLoggingFilter();
   filter.setIncludeQueryString(true);
   filter.setIncludePayload(true);
   filter.setMaxPayloadLength(10000);
   filter.setIncludeHeaders(false);

   return filter;
}
```

