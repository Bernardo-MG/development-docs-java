# Type Erasure

Generics and types and checked at compile time. That means that they won't check types during runtime.

While this makes them more efficient it also means that types can be lost during runtime, and for example a list of Number may end containing Strings.

The erasure is a bit more complex than that, but it means that types should be set explicitly always to avoid problems.

