<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Converters](./ts-utils.converters.md) &gt; [discriminatedObject](./ts-utils.converters.discriminatedobject.md)

## Converters.discriminatedObject() function

Helper to create a [Converter](./ts-utils.converter.md) whhich converts a discriminated object without changing shape.

<b>Signature:</b>

```typescript
export declare function discriminatedObject<T, TD extends string = string, TC = unknown>(discriminatorProp: string, converters: DiscriminatedObjectConverters<T, TD>): Converter<T, TC>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  discriminatorProp | string | Name of the property used to discriminate types. |
|  converters | DiscriminatedObjectConverters&lt;T, TD&gt; | [String-keyed record of converters](./ts-utils.converters.discriminatedobjectconverters.md) to invoke, where each key corresponds to a value of the discriminator property. |

<b>Returns:</b>

[Converter](./ts-utils.converter.md)<!-- -->&lt;T, TC&gt;

A [Converter](./ts-utils.converter.md) which converts the corresponding discriminated object.

## Remarks

Takes the name of the discriminator property and a [string-keyed Record of converters](./ts-utils.converters.discriminatedobjectconverters.md)<!-- -->. During conversion, the resulting [Converter](./ts-utils.converter.md) invokes the converter from `converters` that corresponds to the value of the discriminator property in the source object.

If the source is not an object, the discriminator property is missing, or the discriminator has a value not present in the converters, conversion fails and returns [Failure](./ts-utils.failure.md) with more information.

