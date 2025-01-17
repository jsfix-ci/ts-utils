<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [failWithDetail](./ts-utils.failwithdetail.md)

## failWithDetail() function

Returns [DetailedFailure&lt;T, TD&gt;](./ts-utils.detailedfailure.md) with a supplied error message and detail.

<b>Signature:</b>

```typescript
export declare function failWithDetail<T, TD>(message: string, detail: TD): DetailedFailure<T, TD>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  message | string | The error message to be returned. |
|  detail | TD | The event detail to be returned. |

<b>Returns:</b>

[DetailedFailure](./ts-utils.detailedfailure.md)<!-- -->&lt;T, TD&gt;

An [DetailedFailure&lt;T, TD&gt;](./ts-utils.detailedfailure.md) with the supplied error message and detail.

