<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [BaseConverter](./ts-utils.baseconverter.md) &gt; [withBrand](./ts-utils.baseconverter.withbrand.md)

## BaseConverter.withBrand() method

returns a converter which adds a brand to the type to prevent mismatched usage of simple types.

<b>Signature:</b>

```typescript
withBrand<B extends string>(brand: B): Converter<Brand<T, B>, TC>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  brand | B | The brand to be applied to the result value. |

<b>Returns:</b>

[Converter](./ts-utils.converter.md)<!-- -->&lt;[Brand](./ts-utils.brand.md)<!-- -->&lt;T, B&gt;, TC&gt;

A [Converter](./ts-utils.converter.md) returning `Brand<T, B>`<!-- -->.

