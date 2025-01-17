<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [ExtendedArray](./ts-utils.extendedarray.md) &gt; [single](./ts-utils.extendedarray.single.md)

## ExtendedArray.single() method

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Determines if this array contains exactly one element which matches a supplied predicate.

<b>Signature:</b>

```typescript
single(predicate?: (item: T) => boolean): Result<T>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  predicate | (item: T) =&gt; boolean | The predicate function to be applied. |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;T&gt;

Returns [Success&lt;T&gt;](./ts-utils.success.md) with the single matching result if exactly one item matches `predicate`<!-- -->. Returns [Failure](./ts-utils.failure.md) with an error message if there are no matches or more than one match.

