<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [mapToRecord](./ts-utils.maptorecord.md)

## mapToRecord() function

Applies a factory method to convert a `Map<TK, TS>` into a `Record<TK, TD>`<!-- -->.

<b>Signature:</b>

```typescript
export declare function mapToRecord<TS, TD, TK extends string = string>(src: Map<TK, TS>, factory: KeyedThingFactory<TS, TD, TK>): Result<Record<TK, TD>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  src | Map&lt;TK, TS&gt; | The <code>Map</code> object to be converted. |
|  factory | KeyedThingFactory&lt;TS, TD, TK&gt; | The factory method used to convert elements. |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;Record&lt;TK, TD&gt;&gt;

[Success](./ts-utils.success.md) with the resulting `Record<TK, TD>` if conversion succeeds, or [Failure](./ts-utils.failure.md) with an error message if an error occurs.

