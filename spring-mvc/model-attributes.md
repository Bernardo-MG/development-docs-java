# Model Attributes

## Initialize the DTO

```java
@ModelAttribute(ExampleEntityViewConstants.BEAN_FORM)
public final ExampleEntityForm getEntityForm() {
    return new ExampleEntityForm();
}
```

## Mapping a Form into the DTO

```java
@PostMapping
public final String saveEntity(final ModelMap model,
        @ModelAttribute(ExampleEntityViewConstants.BEAN_FORM) @Valid final ExampleEntityForm form,
        final BindingResult bindingResult, final HttpSession session)
```

