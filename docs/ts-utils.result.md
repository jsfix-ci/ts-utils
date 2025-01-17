<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Result](./ts-utils.result.md)

## Result type

Represents the [result](./ts-utils.iresult.md) of some operation or sequence of operations.

<b>Signature:</b>

```typescript
export declare type Result<T> = Success<T> | Failure<T>;
```
<b>References:</b> [Success](./ts-utils.success.md)<!-- -->, [Failure](./ts-utils.failure.md)

## Remarks

[Success&lt;T&gt;](./ts-utils.success.md) and [Failure&lt;T&gt;](./ts-utils.failure.md) share the common contract [IResult](./ts-utils.iresult.md)<!-- -->, enabling comingled discriminated usage.

