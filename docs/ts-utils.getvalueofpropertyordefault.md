<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [getValueOfPropertyOrDefault](./ts-utils.getvalueofpropertyordefault.md)

## getValueOfPropertyOrDefault() function

Gets the value of a property specified by key from an arbitrary object, or a default value if the property does not exist.

<b>Signature:</b>

```typescript
export declare function getValueOfPropertyOrDefault<T extends object>(key: string | number | symbol, item: T, defaultValue?: unknown): unknown | undefined;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  key | string \| number \| symbol | The key specifying the property to be retrieved. |
|  item | T | The object from which the property is to be retrieved. |
|  defaultValue | unknown | An optional default value to be returned if the property is not present (default <code>undefined</code>). |

<b>Returns:</b>

unknown \| undefined

The value of the requested property, or the default value if the requested property does not exist.

