<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [RangeOf](./ts-utils.rangeof.md) &gt; [findTransition](./ts-utils.rangeof.findtransition.md)

## RangeOf.findTransition() method

Finds the transition value that would bring a supplied value `t` into range.

<b>Signature:</b>

```typescript
findTransition(t: T): T | undefined;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  t | T | The value to be tested. |

<b>Returns:</b>

T \| undefined

The minimum extent of the range if `t` is below the range or the maximum extent of the range if `t` is above the range. Returns `undefined` if `t` already falls within the range.

