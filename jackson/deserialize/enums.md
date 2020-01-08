# Enums

```java
public enum ValueEnum {

   DEFAULT(0);

   private Integer value;

   private ValueEnum(final Integer val)
   {
      value = val;
   }

   @JsonCreator
   public static ValueEnum valueOfJson(final String value)
   {
      final ValueEnum parsed;

	    // Transform from JSON to enum

      return parsed;
   }

   @JsonValue
   public Integer getValue()
   {
      return value;
   }

}
```

