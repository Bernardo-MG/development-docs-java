# Setting Up

## Plugin

Inside the POM:

```markup
<build>
   <plugins>
      <plugin>
         <!-- Site -->
         <!-- Generates the Maven Site -->
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-site-plugin</artifactId>
         <dependencies>
            <dependency>
               <!-- Docs Maven Skin -->
               <groupId>com.bernardomg.maven.skins</groupId>
               <artifactId>docs-maven-skin</artifactId>
               <version>${site.skin.version}</version>
            </dependency>
         </dependencies>
      </plugin>
   </plugins>
</build>
```

## Site Skin

Inside /src/site/site.xml:

```markup
<skin>
   <groupId>com.bernardomg.maven.skins</groupId>
   <artifactId>docs-maven-skin</artifactId>
   <version>${site.skin.version}</version>
</skin>
```

## Additional Configuration

Add an index file at src/site/markdown/index.md.

Then check any additional configuration which the skin may have.

## Aggregating Reports

This is for multimodule projects, where reports are generated for each module. These reports may be aggregated, but it is not recommended, as Maven has problems generating aggregated reports.

Report aggregation can be activating by settingthis property:

```markup
<properties>
   <aggregate>true</aggregate>
</properties>
```

### Plugins configuration

```markup
<plugin>
   <!-- Javadoc -->
   <!-- Handles the Javadocs. -->
   <groupId>org.apache.maven.plugins</groupId>
   <artifactId>maven-javadoc-plugin</artifactId>
   <executions>
      <execution>
         <id>aggregate-javadoc</id>
         <goals>
            <goal>aggregate</goal>
         </goals>
         <phase>site</phase>
      </execution>
   </executions>
</plugin>
```

