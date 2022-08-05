<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Validation](./ts-utils.validation.md) &gt; [Constraint](./ts-utils.validation.constraint.md)

## Validation.Constraint type

A [Constraint&lt;T&gt;](./ts-utils.validation.constraint.md) function returns `true` if the supplied value meets the constraint. Can return [Failure](./ts-utils.failure.md) with an error message or simply return `false` for a default message.

<b>Signature:</b>

```typescript
export declare type Constraint<T> = (val: T) => boolean | Failure<T>;
```
<b>References:</b> [Failure](./ts-utils.failure.md)
