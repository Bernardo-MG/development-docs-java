# Method Security

## XML

```markup
<global-method-security pre-post-annotations="enabled" />
```

## Configuration Class

```java
@EnableGlobalMethodSecurity(prePostEnabled = true, mode = AdviceMode.ASPECTJ)
```

