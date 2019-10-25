# Component Scanning

## Configuration Class

```java
@Configuration
@ComponentScan({ "com.package.repository" })
public class RepositoryScanningConfig
{

}
```

## XML

```markup
<context:component-scan base-package="com.package.repository" />
```



