<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [DetailedSuccess](./ts-utils.detailedsuccess.md) &gt; [onFailure](./ts-utils.detailedsuccess.onfailure.md)

## DetailedSuccess.onFailure() method

Propagates this [DetailedSuccess](./ts-utils.detailedsuccess.md)<!-- -->.

<b>Signature:</b>

```typescript
onFailure(_cb: DetailedFailureContinuation<T, TD>): DetailedResult<T, TD>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  \_cb | [DetailedFailureContinuation](./ts-utils.detailedfailurecontinuation.md)<!-- -->&lt;T, TD&gt; | [Failure callback](./ts-utils.detailedfailurecontinuation.md) to be called on a [DetailedResult](./ts-utils.detailedresult.md) in case of failure (ignored). |

<b>Returns:</b>

[DetailedResult](./ts-utils.detailedresult.md)<!-- -->&lt;T, TD&gt;

`this`

## Remarks

Failure does not mutate return type so we can return this event directly.

