<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Converters](./ts-utils.converters.md) &gt; [enumeratedValue](./ts-utils.converters.enumeratedvalue.md)

## Converters.enumeratedValue() function

Helper function to create a [Converter](./ts-utils.converter.md) which converts `unknown` to one of a set of supplied enumerated values. Anything else fails.

<b>Signature:</b>

```typescript
export declare function enumeratedValue<T>(values: T[]): Converter<T, T[]>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  values | T\[\] | Array of allowed values. |

<b>Returns:</b>

[Converter](./ts-utils.converter.md)<!-- -->&lt;T, T\[\]&gt;

A new [Converter](./ts-utils.converter.md) returning `<T>`<!-- -->.

## Remarks

Allowed enumerated values can also be supplied as context at conversion time.
