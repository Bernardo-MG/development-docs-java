# WebJars

[Webjars](http://www.webjars.org/) are frontend dependencies packaged into Jars.

The downside is that they require a specific framework, such as Spring or Play, to be usable. Check their documentation for more details.

## Minification

To minify JS and CSS files use the [Minify Maven Plugin](http://samaxes.github.io/minify-maven-plugin/).

### CSS

```markup
<plugin>
   <!-- Minify -->
   <!-- Minifies files. -->
   <groupId>com.samaxes.maven</groupId>
   <artifactId>minify-maven-plugin</artifactId>
   <executions>
      <execution>
         <id>minify-css</id>
         <phase>package</phase>
         <configuration>
            <cssSourceDir>resources/css</cssSourceDir>
            <cssSourceIncludes>
               <cssSourceInclude>**</cssSourceInclude>
            </cssSourceIncludes>
            <cssFinalFile>style.css</cssFinalFile>
         </configuration>
         <goals>
            <goal>minify</goal>
         </goals>
      </execution>
   </executions>
</plugin>
```

### Javascript

```markup
<plugin>
   <!-- Minify -->
   <!-- Minifies files. -->
   <groupId>com.samaxes.maven</groupId>
   <artifactId>minify-maven-plugin</artifactId>
   <executions>
      <execution>
         <id>minify-js</id>
         <configuration>
            <jsSourceIncludes>
               <jsSourceInclude>**</jsSourceInclude>
            </jsSourceIncludes>
            <jsSourceExcludes>
               <jsSourceExclude>initialize.js</jsSourceExclude>
            </jsSourceExcludes>
            <jsFinalFile>scripts.js</jsFinalFile>
         </configuration>
         <goals>
            <goal>minify</goal>
         </goals>
      </execution>
   </executions>
</plugin>
```

## Javascript validation

The [JSHint plugin](https://github.com/cjdev/jshint-mojo) to validate Javascript files, but it is no longer supported.

```markup
<plugin>
   <!-- JSHint -->
   <!-- Validates Javascript files. -->
   <groupId>com.cj.jshintmojo</groupId>
   <artifactId>jshint-maven-plugin</artifactId>
   <executions>
      <execution>
         <id>jshint</id>
         <phase>test</phase>
         <goals>
            <goal>lint</goal>
         </goals>
      </execution>
   </executions>
   <configuration>
      <options>maxdepth:3,latedef,nonew,jquery</options>
      <directories>
         <directory>src/main/webapp/resources/js</directory>
      </directories>
      <reporter>checkstyle</reporter>
      <reportFile>target/jshint.xml</reportFile>
      <failOnError>true</failOnError>
   </configuration>
</plugin>
```

