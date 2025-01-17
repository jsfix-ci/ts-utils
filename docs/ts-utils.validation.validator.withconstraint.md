<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Validation](./ts-utils.validation.md) &gt; [Validator](./ts-utils.validation.validator.md) &gt; [withConstraint](./ts-utils.validation.validator.withconstraint.md)

## Validation.Validator.withConstraint() method

Creates an [in-place validator](./ts-utils.validation.validator.md) which is derived from this one but which applies additional constraints.

<b>Signature:</b>

```typescript
withConstraint(constraint: Constraint<T>, trait?: ConstraintTrait): Validator<T, TC>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  constraint | Constraint&lt;T&gt; | the constraint to be applied |
|  trait | ConstraintTrait | As optional [ConstraintTrait](./ts-utils.validation.constrainttrait.md) to be applied to the resulting [Validator](./ts-utils.validation.validator.md)<!-- -->. |

<b>Returns:</b>

Validator&lt;T, TC&gt;

A new [Validator](./ts-utils.validation.validator.md)<!-- -->.

