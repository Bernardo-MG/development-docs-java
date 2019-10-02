# Setting Up

## Authentication Manager

This will take care of authenticating users.

```markup
<authentication-manager>
   <authentication-provider user-service-ref="userDetailsService">
      <!-- <password-encoder ref="passwordEncoder" /> -->
   </authentication-provider>
</authentication-manager>
```

## Method Security

To activate security annotations:

```markup
<global-method-security pre-post-annotations="enabled" />
```

```java
@EnableGlobalMethodSecurity(prePostEnabled = true)
```

