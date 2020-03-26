# Validator

Java offers a validator interface as javax.validation.Validator.

## Usage

```java
Collection<ConstraintViolation<String>> constraintViolations;

constraintViolations = validator.validate(object);
```

### Validating groups

```java
constraintViolations = validator.validate(object, UpdateValidationGroup.class)
```

