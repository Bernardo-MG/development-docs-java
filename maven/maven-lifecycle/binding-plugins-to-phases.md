# Binding Plugins to Phases

Plugins are bond to phases:

```markup
<plugin>
   <groupId>org.apache.maven.plugins</groupId>
   <artifactId>maven-failsafe-plugin</artifactId>
   <executions>
      <execution>
         <id>failsafe-verify</id>
         <goals>
            <goal>verify</goal>
         </goals>
      </execution>
   </executions>
</plugin>
```

