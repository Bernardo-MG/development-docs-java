# Maven Lifecycle

To understand Maven one first needs to understand the [Maven lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)

## Calling Goals and Phases

Not all phases are meant to be called by the user, as some are hooks for the plugins.

The main phases, which can be used, are:

* validate
* compile
* test
* package
* verify
* install
* deploy

Prefixed phases, starting with pre-, post- and process- should be avoided. These are not meant to be called by users and may cause problems.

## More Information

* [Introduction to the Build Lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)

