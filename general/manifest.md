# Manifest

JARs contain a description of its content in the manifest file. This can be used to describe the generated artifact, by indicating the main executable class, the included dependencies or version information.

The manifest should be generated by a project manager tool, and not manually.

It is located in the META-INF/MANIFEST.MF path, and is a text file which can be opened with any editor.

```text
Manifest-Version: 1.0
Implementation-Title: Dice Notation Tools for Java
Package: com.bernardomg.tabletop
Implementation-Version: 1.1.0-SNAPSHOT
Built-By: Bernardo
Specification-Vendor: Bernardo Martínez Garrido
Specification-Title: Dice Notation Tools for Java
Implementation-Vendor-Id: com.bernardomg.tabletop
Class-Path: antlr4-4.7.jar antlr4-runtime-4.7.jar antlr-runtime-3.5.2.
 jar ST4-4.0.8.jar org.abego.treelayout.core-1.0.3.jar javax.json-1.0.
 4.jar icu4j-58.2.jar guava-23.5-jre.jar jsr305-1.3.9.jar checker-qual
 -2.0.0.jar error_prone_annotations-2.0.18.jar j2objc-annotations-1.1.
 jar animal-sniffer-annotations-1.14.jar
url: https://github.com/bernardo-mg/dice-notation-java
Implementation-Vendor: Bernardo Martínez Garrido
name: com/bernardomg/tabletop/dice
Created-By: Apache Maven 3.3.9
Build-Jdk: 1.8.0_112
Specification-Version: 1.1
Implementation-URL: https://github.com/bernardo-mg/dice-notation-java
```

Manifest are required by some services, such as Heroku, but in most situations a basic one will suffice.

## More Information

* [Working with Manifest Files: The Basics](https://docs.oracle.com/javase/tutorial/deployment/jar/manifestindex.html)

