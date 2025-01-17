<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Converters](./ts-utils.converters.md) &gt; [ObjectConverter](./ts-utils.converters.objectconverter.md) &gt; [partial](./ts-utils.converters.objectconverter.partial.md)

## Converters.ObjectConverter.partial() method

Creates a new [ObjectConverter](./ts-utils.converters.objectconverter.md) derived from this one but with new optional properties as specified by a supplied [ObjectConverterOptions&lt;T&gt;](./ts-utils.converters.objectconverteroptions.md)<!-- -->.

<b>Signature:</b>

```typescript
partial(options: ObjectConverterOptions<T>): ObjectConverter<Partial<T>, TC>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  options | ObjectConverterOptions&lt;T&gt; | The [options](./ts-utils.converters.objectconverteroptions.md) to be applied to the new converter. |

<b>Returns:</b>

ObjectConverter&lt;Partial&lt;T&gt;, TC&gt;

A new [ObjectConverter](./ts-utils.converters.objectconverter.md) with the additional optional source properties. 

