<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@fgv/ts-utils](./ts-utils.md) &gt; [Validation](./ts-utils.validation.md) &gt; [Validators](./ts-utils.validation.validators.md) &gt; [object](./ts-utils.validation.validators.object.md)

## Validation.Validators.object() function

Helper function to create a [ObjectValidator](./ts-utils.validation.classes.objectvalidator.md) which validates an object in place.

<b>Signature:</b>

```typescript
export declare function object<T, TC>(fields: FieldValidators<T, TC>, params?: Omit<ObjectValidatorConstructorParams<T, TC>, 'fields'>): ObjectValidator<T, TC>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  fields | FieldValidators&lt;T, TC&gt; | A [field validator definition](./ts-utils.validation.classes.fieldvalidators.md) describing the validations to be applied. |
|  params | Omit&lt;ObjectValidatorConstructorParams&lt;T, TC&gt;, 'fields'&gt; | Optional [parameters](./ts-utils.validation.classes.objectvalidatorconstructorparams.md) to refine the behavior of the resulting [validator](./ts-utils.validation.validator.md)<!-- -->. |

<b>Returns:</b>

ObjectValidator&lt;T, TC&gt;

A new [Validator](./ts-utils.validation.validator.md) which validates the desired object in place.

