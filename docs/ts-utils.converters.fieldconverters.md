<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Converters](./ts-utils.converters.md) &gt; [FieldConverters](./ts-utils.converters.fieldconverters.md)

## Converters.FieldConverters type

Per-property converters for each of the properties in type T.

<b>Signature:</b>

```typescript
export declare type FieldConverters<T, TC = unknown> = {
    [key in keyof T]: Converter<T[key], TC>;
};
```
<b>References:</b> [Converter](./ts-utils.converter.md)

## Remarks

Used to construct a [ObjectConverter](./ts-utils.converters.objectconverter.md)

