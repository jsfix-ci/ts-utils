<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Csv](./ts-utils.csv.md) &gt; [readCsvFileSync](./ts-utils.csv.readcsvfilesync.md)

## Csv.readCsvFileSync() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Reads a CSV file from a supplied path.

<b>Signature:</b>

```typescript
export declare function readCsvFileSync(srcPath: string): Result<unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  srcPath | string | Source path from which the file is read. |

<b>Returns:</b>

[Result](./ts-utils.result.md)<!-- -->&lt;unknown&gt;

The contents of the file.

