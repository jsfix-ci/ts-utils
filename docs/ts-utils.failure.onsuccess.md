<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Failure](./ts-utils.failure.md) &gt; [onSuccess](./ts-utils.failure.onsuccess.md)

## Failure.onSuccess() method

Calls a supplied [success continuation](./ts-utils.successcontinuation.md) if the operation was a success.

<b>Signature:</b>

```typescript
onSuccess<TN>(_: SuccessContinuation<T, TN>): Result<TN>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  \_ | [SuccessContinuation](./ts-utils.successcontinuation.md)<!-- -->&lt;T, TN&gt; |  |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;TN&gt;

If this operation was successful, returns the value returned by the [success continuation](./ts-utils.successcontinuation.md)<!-- -->. If this result failed, propagates the error message from this failure.

## Remarks

The [success continuation](./ts-utils.successcontinuation.md) might return a different result type than [IResult](./ts-utils.iresult.md) on which it is invoked. This enables chaining of operations with heterogenous return types.
