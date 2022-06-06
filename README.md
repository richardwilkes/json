# json
This is a clone of the encoding/json package with added support for:

- passing a context in both encode and decode. For those places where it is needed, this requires implementing new `MarshalerWithContext` and `UnmarshalerWithContext` interfaces to receive the context.
- deciding whether to omit data by implementing the `Omitter` interface, if present (this in addition to the old way).
- reading data with an alternate tag, useful when a tag name has changed in a newer format but you still want to load older data.
