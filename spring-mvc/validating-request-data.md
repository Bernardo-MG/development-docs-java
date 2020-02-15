# Validating Request Data

```java
public final String create(@ModelAttribute("form") @Validated(Creation.class) final UserForm form,
            final BindingResult bindingResult)
```

```java
public final String create(@ModelAttribute("form") Valid @Validated(Creation.class) final UserForm form)
```

