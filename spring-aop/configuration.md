# Configuration

## Aspect



```java
@Aspect
public class CustomAspect
{

   // Code

}
```

## XML

```markup
<beans xmlns="http://www.springframework.org/schema/beans"
   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:context="http://www.springframework.org/schema/context"
   xmlns:aop="http://www.springframework.org/schema/aop"
   xsi:schemaLocation="http://www.springframework.org/schema/beans
      http://www.springframework.org/schema/beans/spring-beans.xsd
      http://www.springframework.org/schema/context 
      http://www.springframework.org/schema/context/spring-context.xsd
      http://www.springframework.org/schema/aop 
      http://www.springframework.org/schema/aop/spring-aop-4.3.xsd">

   <!-- Activates aspects -->
   <aop:aspectj-autoproxy />

   <!-- Scans for aspects -->
   <context:component-scan base-package="com.bernardomg.example.test.**.aspect" />

</beans>
```

## Configuration Class

```java
@Configuration
@EnableAspectJAutoProxy
public class AppConfig {

}
```

