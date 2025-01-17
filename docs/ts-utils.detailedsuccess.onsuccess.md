<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [DetailedSuccess](./ts-utils.detailedsuccess.md) &gt; [onSuccess](./ts-utils.detailedsuccess.onsuccess.md)

## DetailedSuccess.onSuccess() method

Invokes the supplied [success callback](./ts-utils.detailedsuccesscontinuation.md) and propagates its returned [DetailedResult&lt;TN, TD&gt;](./ts-utils.detailedresult.md)<!-- -->.

<b>Signature:</b>

```typescript
onSuccess<TN>(cb: DetailedSuccessContinuation<T, TD, TN>): DetailedResult<TN, TD>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  cb | [DetailedSuccessContinuation](./ts-utils.detailedsuccesscontinuation.md)<!-- -->&lt;T, TD, TN&gt; | The [success callback](./ts-utils.detailedsuccesscontinuation.md) to be invoked. |

<b>Returns:</b>

[DetailedResult](./ts-utils.detailedresult.md)<!-- -->&lt;TN, TD&gt;

The [DetailedResult&lt;T, TD&gt;](./ts-utils.detailedresult.md) returned by the success callback.

## Remarks

The success callback mutates the return type from `<T>` to `<TN>`<!-- -->.

