<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Infer](./ts-utils.infer.md)

## Infer type

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Infers the type that will be returned by an intstantiated converter. Works for complex as well as simple types.

<b>Signature:</b>

```typescript
export declare type Infer<TCONV> = TCONV extends Converter<infer TTO> ? InnerInferredType<TTO> : never;
```
<b>References:</b> [Converter](./ts-utils.converter.md)

## Example

`Infer<typeof Converters.mapOf(Converters.stringArray)>` is `Map<string, string[]>`

