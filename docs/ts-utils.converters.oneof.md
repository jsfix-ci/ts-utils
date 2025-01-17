<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Converters](./ts-utils.converters.md) &gt; [oneOf](./ts-utils.converters.oneof.md)

## Converters.oneOf() function

A helper function to create a [Converter](./ts-utils.converter.md) for polymorphic values. Returns a converter which Invokes the wrapped converters in sequence, returning the first successful result. Returns an error if none of the supplied converters can convert the value.

<b>Signature:</b>

```typescript
export declare function oneOf<T, TC = unknown>(converters: Array<Converter<T, TC>>, onError?: OnError): Converter<T, TC>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  converters | Array&lt;[Converter](./ts-utils.converter.md)<!-- -->&lt;T, TC&gt;&gt; | An ordered list of [converters](./ts-utils.converter.md) to be considered. |
|  onError | OnError | Specifies treatment of unconvertable elements. |

<b>Returns:</b>

[Converter](./ts-utils.converter.md)<!-- -->&lt;T, TC&gt;

A new [Converter](./ts-utils.converter.md) which yields a value from the union of the types returned by the wrapped converters.

## Remarks

If `onError` is `ignoreErrors` (default), then errors from any of the converters are ignored provided that some converter succeeds. If onError is `failOnError`<!-- -->, then an error from any converter fails the entire conversion.

