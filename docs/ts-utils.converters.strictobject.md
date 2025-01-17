<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Converters](./ts-utils.converters.md) &gt; [strictObject](./ts-utils.converters.strictobject.md)

## Converters.strictObject() function

Helper function to create a [ObjectConverter](./ts-utils.converters.objectconverter.md) which converts an object without changing shape, a [FieldConverters&lt;T&gt;](./ts-utils.converters.fieldconverters.md) and an optional [StrictObjectConverterOptions&lt;T&gt;](./ts-utils.converters.strictobjectconverteroptions.md) to further refine conversion behavior.

<b>Signature:</b>

```typescript
export declare function strictObject<T>(properties: FieldConverters<T>, options?: StrictObjectConverterOptions<T>): ObjectConverter<T>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  properties | FieldConverters&lt;T&gt; | An object containing defining the shape and converters to be applied. |
|  options | StrictObjectConverterOptions&lt;T&gt; | An optional |

<b>Returns:</b>

ObjectConverter&lt;T&gt;

A new [ObjectConverter](./ts-utils.converters.objectconverter.md) which applies the specified conversions. 

## Remarks

Fields that succeed but convert to undefined are omitted from the result object but do not fail the conversion.

The conversion fails if any unexpected fields are encountered.

