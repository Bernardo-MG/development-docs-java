# Executable JAR

## Plugin Configuration

In this example the Main executable class is located at org.company.Main.

```markup
<build>
   <plugins>
      <plugin>
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-compiler-plugin</artifactId>
         <configuration>
            <mainClass>org.company.Main</mainClass>
         </configuration>
      </plugin>
      <plugin>
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-jar-plugin</artifactId>
         <configuration>
            <archive>
               <index>true</index>
               <manifest>
                  <classpathPrefix>lib/</classpathPrefix>
                  <addClasspath>true</addClasspath>
                  <mainClass>org.company.Main</mainClass>
               </manifest>
            </archive>
         </configuration>
      </plugin>
      <plugin>
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-dependency-plugin</artifactId>
         <executions>
            <execution>
               <id>copy-dependencies</id>
               <phase>package</phase>
               <goals>
                  <goal>copy-dependencies</goal>
               </goals>
               <configuration>
                  <includeScope>runtime</includeScope>
                  <outputDirectory>${project.build.directory}/lib</outputDirectory>
                  <overWriteReleases>true</overWriteReleases>
                  <overWriteSnapshots>true</overWriteSnapshots>
                  <overWriteIfNewer>true</overWriteIfNewer>
               </configuration>
            </execution>
         </executions>
      </plugin>
      <plugin>
         <groupId>org.codehaus.mojo</groupId>
         <artifactId>exec-maven-plugin</artifactId>
         <executions>
            <execution>
               <goals>
                  <goal>java</goal>
               </goals>
            </execution>
         </executions>
         <configuration>
            <mainClass>org.company.Main</mainClass>
         </configuration>
      </plugin>
   </plugins>
</build>
```

