# Conditional Configuration

## Conditional by Property

If the property matches the defined value then the configuration is applied.

```java
@Configuration
@ConditionalOnProperty(name = "property.name", matchIfMissing = false, havingValue = "true")
public class ConfigClass
```

| Argument | Usage |
| :--- | :--- |
| havingValue | The value required to activate the condition |
| matchIfMissing | If true, the condition activates when the property is not defined |

## Conditional by Condition Class

When the condition returns true then the configuration is applied.

```java
@Configuration
@Conditional(ConfigurationCondition.class)
public class ConfigClass
```

```java
public class ConfigurationCondition implements Condition
{

   @Override
   public boolean matches(final ConditionContext context, final AnnotatedTypeMetadata metadata)
   {
      // Code
   }

}
```

## Conditional by Bean

The bean is loaded only if the referenced bean has been loaded:

```java
@Bean
@ConditionalOnBean(name="mainBean")
public Component component(){
   return new Component();
}
```

The bean is loaded only if the referenced bean has NOT been loaded:

```java
@Bean
@ConditionalOnMissingBean(name="mainBean")
public Placeholder placeholder(){
   return new Placeholder();
}
```

## Conditional by Class

The bean is loaded only if the class is in the classpath:

```java
@Bean
@ConditionalOnClass(name="com.path.Driver")
public Driver driver(){
   return new Driver();
}
```

The bean is loaded only if the class is missing from the classpath:

```java
@Bean
@ConditionalOnMissingClass(name="com.path.Driver")
public AnotherDriver driver(){
   return new AnotherDriver ();
}
```

