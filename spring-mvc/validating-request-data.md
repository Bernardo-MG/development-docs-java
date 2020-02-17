# Validating Request Data

## Java Validation Annotations

Spring supports the Java Validation API:

```java
public final String create(@ModelAttribute("form") @Validated(Creation.class) final UserForm form,
            final BindingResult bindingResult) {
   if (bindingResult.hasErrors()) {
      // Handle error
   }

   // Return response
}
```

## Spring Annotations

Using Spring any validation failure will throw a MethodArgumentNotValidException. The only requirement is adding the @Valid annotation.

```java
public final String create(@ModelAttribute("form") @Valid @Validated(Creation.class) final UserForm form)
```

