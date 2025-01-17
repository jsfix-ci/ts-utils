<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [ExtendedArray](./ts-utils.extendedarray.md) &gt; [atLeastOne](./ts-utils.extendedarray.atleastone.md)

## ExtendedArray.atLeastOne() method

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Returns an array containing all elements of an [ExtendedArray](./ts-utils.extendedarray.md)<!-- -->. Fails with an error message if the array is empty.

<b>Signature:</b>

```typescript
atLeastOne(failMessage?: string): Result<T[]>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  failMessage | string | Optional message to be displayed in the event of failure. |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;T\[\]&gt;

Returns [Success&lt;T\[\]&gt;](./ts-utils.success.md) with a new (non-extended) `Array` containing the elements of this array, or [Failure](./ts-utils.failure.md) with an error message if the array is empty.

