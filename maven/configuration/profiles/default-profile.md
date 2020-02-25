# Forcing an Active Profile

## Activation Property

```markup
<profile>
   <!-- Active on Eclipse -->
   <id>eclipse</id>
   <activation>
      <property>
         <name>m2e.version</name>
      </property>
   </activation>
</profile>
```

## Settings File

```markup
<settings>
   <activeProfiles>
      <activeProfile>profileName</activeProfile>
   </activeProfiles>
</settings>
```

