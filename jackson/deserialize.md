# Deserialize

### Annotation

```java
@JsonDeserialize(as = CarImpl.class)
public interface Car
```

## Creator

```java
public enum TipoCalculoMedia {

   @JsonCreator
   public static EnumValue valueOfJson(final String value) {
      if (StringUtils.isBlank(value)) {
         return EnumValue.DEFAULT;
      }
   
      return valueOf(Integer.parseInt(value));
   }

}
```

