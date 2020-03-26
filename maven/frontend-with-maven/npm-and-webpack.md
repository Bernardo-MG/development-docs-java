# npm and Webpack

Some project may have advanced requirements, such as additional dependencies, which only npm and webpack can handle.

For these cases the [Frontend Maven plugin](https://github.com/eirslett/frontend-maven-plugin) can be used.

## npm

```markup
<plugin>
   <!-- Frontend Plugin -->
   <!-- Manages frontend dependencies -->
   <groupId>com.github.eirslett</groupId>
   <artifactId>frontend-maven-plugin</artifactId>
   <configuration>
      <installDirectory>target</installDirectory>
   </configuration>
   <executions>
      <execution>
         <id>node-npm-install</id>
         <goals>
            <goal>install-node-and-npm</goal>
         </goals>
         <configuration>
            <nodeVersion>${plugin.frontend.node.version}</nodeVersion>
            <npmVersion>${plugin.frontend.npm.version}</npmVersion>
         </configuration>
      </execution>
      <execution>
         <id>npm-install</id>
         <goals>
            <goal>npm</goal>
         </goals>
         <configuration>
            <arguments>install</arguments>
         </configuration>
      </execution>
   </executions>
</plugin>
```

It is recommended binding a npm testing script to the testing phase:

```markup
<plugin>
   <!-- Frontend Plugin -->
   <groupId>com.github.eirslett</groupId>
   <artifactId>frontend-maven-plugin</artifactId>
   <executions>
      <execution>
         <id>npm-test</id>
         <goals>
            <goal>npm</goal>
         </goals>
         <phase>test</phase>
         <configuration>
            <arguments>test</arguments>
         </configuration>
      </execution>
   </executions>
</plugin>
```

## npm with webpack

```markup
<plugin>
   <!-- Frontend Plugin -->
   <groupId>com.github.eirslett</groupId>
   <artifactId>frontend-maven-plugin</artifactId>
   <configuration>
      <installDirectory>target</installDirectory>
   </configuration>
   <executions>
      <execution>
         <id>node-npm-install</id>
         <goals>
            <goal>install-node-and-npm</goal>
         </goals>
         <configuration>
            <nodeVersion>${plugin.frontend.node.version}</nodeVersion>
            <npmVersion>${plugin.frontend.npm.version}</npmVersion>
         </configuration>
      </execution>
      <execution>
         <id>npm-install</id>
         <goals>
            <goal>npm</goal>
         </goals>
         <configuration>
            <arguments>install</arguments>
         </configuration>
      </execution>
      <execution>
         <id>webpack</id>
         <goals>
            <goal>webpack</goal>
         </goals>
      </execution>
   </executions>
</plugin>
```

If needed, webpack can receive environmental variables:

```markup
<plugin>
   <!-- Frontend Plugin -->
   <groupId>com.github.eirslett</groupId>
   <artifactId>frontend-maven-plugin</artifactId>
   <executions>
      <execution>
         <id>webpack</id>
         <goals>
            <goal>webpack</goal>
         </goals>
         <configuration>
            <environmentVariables>
               <NODE_ENV>${node.env}</NODE_ENV>
               <APP_VERSION>${node.env.appVersion}</APP_VERSION>
               <APP_ROUTE>${node.env.rootRoute}</APP_ROUTE>
               <REPO_URL>${node.env.repoUrl}</REPO_URL>
               <INPUT_PATH>${node.env.inputPath}</INPUT_PATH>
               <OUTPUT_PATH>${node.env.outputPath}</OUTPUT_PATH>
               <MODULE_PATH>${node.env.modules}</MODULE_PATH>
            </environmentVariables>
         </configuration>
      </execution>
   </executions>
</plugin>
```

