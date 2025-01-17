<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [allSucceed](./ts-utils.allsucceed.md)

## allSucceed() function

Determines if an iterable collection of [Result&lt;T&gt;](./ts-utils.result.md) were all successful.

<b>Signature:</b>

```typescript
export declare function allSucceed<T>(results: Iterable<Result<unknown>>, successValue: T): Result<T>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  results | Iterable&lt;[Result](./ts-utils.result.md)<!-- -->&lt;unknown&gt;&gt; | The collection of [Result&lt;T&gt;](./ts-utils.result.md) to be tested. |
|  successValue | T |  |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;T&gt;

Returns [Success](./ts-utils.success.md) with `true` if all [results](./ts-utils.result.md) are successful. If any are unsuccessful, returns [Failure](./ts-utils.failure.md) with a concatenated summary the error messages from all failed elements.

