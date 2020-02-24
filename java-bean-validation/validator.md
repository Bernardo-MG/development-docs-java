# Validator

Java offers a validator interface.

## Usage

```java
Collection<ConstraintViolation<String>> constraintViolations;

constraintViolations = validator.validate(object);
```

Validating groups:

```java
constraintViolations = validator.validate(object, UpdateValidationGroup.class, CreateValidation
```

