# Model Attributes

## Initialize the DTO

```java
@ModelAttribute(ExampleEntityViewConstants.BEAN_FORM)
public final ExampleEntityForm getEntityForm() {
    return new DefaultExampleEntityForm();
}
```

## Mapping a Form into the DTO

```java
@PostMapping
public final String saveEntity(@ModelAttribute("formBean") final ExampleEntityForm form)
```

