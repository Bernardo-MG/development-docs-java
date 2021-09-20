# Annotation Extension

```java
@Retention(RetentionPolicy.RUNTIME)
@ExtendWith(CleanupExtension.class)
@Target({ ElementType.TYPE, ElementType.METHOD })
public @interface DataCleanup {

}
```

```java
public final class CleanupExtension
        implements BeforeEachCallback, AfterEachCallback {

    public CleanupExtension() {
        super();
    }

    @Override
    public final void afterEach(final ExtensionContext context)
            throws Exception {
        cleanup(context);
    }

    @Override
    public final void beforeEach(final ExtensionContext context)
            throws Exception {
        cleanup(context);
    }

    public final void cleanup(final ExtensionContext context) throws Exception {
        // Clean up operation
    }

}
```

