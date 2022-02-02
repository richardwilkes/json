# json
This is a clone of the encoding/json package with some extra options:

- Support for passing a context in both encode and decode. This requires implementing new `MarshalerWithContext` and `UnmarshalerWithContext` interfaces to receive the context.
- Support for deciding whether to omit data by implementing the `Omitter` interface.
