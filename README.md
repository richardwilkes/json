# json

This is a clone of the encoding/json package with added support for:

- passing a context in both encode and decode. For those places where it is needed, this requires implementing new
  `MarshalerWithContext` and `UnmarshalerWithContext` interfaces to receive the context.
- reading data with an alternate tag, useful when a tag name has changed in a newer format but you still want to load
  older data.

The `Omitter` interface support that was present in v0.3.0 and earlier has been removed with the v0.4.0 release, in
preference to the `omitZero` tag and `IsZero` interface support that was added in Go 1.24.0.
