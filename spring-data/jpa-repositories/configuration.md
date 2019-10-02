# Configuration

## Setting Up Repositories

Repositories need to be loaded through an specific configuration:

```java
<jpa:repositories base-package="com.project.**.repository" />
```

This can be done with configuration classes:

```java
@EnableJpaRepositories
class Config {}
```

