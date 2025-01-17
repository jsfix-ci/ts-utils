<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [populateObject](./ts-utils.populateobject.md)

## populateObject() function

Populates an an object based on a prototype full of field initializers that return [Result&lt;T\[key\]&gt;](./ts-utils.result.md)<!-- -->. Returns [Success](./ts-utils.success.md) with the populated object if all initializers succeed, or [Failure](./ts-utils.failure.md) with a concatenated list of all error messages.

<b>Signature:</b>

```typescript
export declare function populateObject<T>(initializers: FieldInitializers<T>, order?: (keyof T)[]): Result<T>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  initializers | [FieldInitializers](./ts-utils.fieldinitializers.md)<!-- -->&lt;T&gt; | An object with the shape of the target but with initializer functions for each property. |
|  order | (keyof T)\[\] |  |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;T&gt;

