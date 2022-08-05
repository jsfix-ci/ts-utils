## API Report File for "@fgv/ts-utils"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public
export function allSucceed<T>(results: Iterable<Result<unknown>>, successValue: T): Result<T>;

// Warning: (ae-forgotten-export) The symbol "OnError" needs to be exported by the entry point index.d.ts
//
// @public
function arrayOf<T, TC = undefined>(converter: Converter<T, TC>, onError?: OnError_2): Converter<T[], TC>;

declare namespace Base {
    export {
        ValidatorFunc,
        GenericValidatorConstructorParams,
        GenericValidator
    }
}

// @public
export class BaseConverter<T, TC = undefined> implements Converter<T, TC> {
    constructor(converter: (from: unknown, self: Converter<T, TC>, context?: TC) => Result<T>, defaultContext?: TC, traits?: ConverterTraits);
    get brand(): string | undefined;
    // @internal (undocumented)
    protected _brand?: string;
    // @internal (undocumented)
    protected _context(supplied?: TC): TC | undefined;
    convert(from: unknown, context?: TC): Result<T>;
    // Warning: (ae-forgotten-export) The symbol "OnError" needs to be exported by the entry point index.d.ts
    convertOptional(from: unknown, context?: TC, onError?: OnError): Result<T | undefined>;
    // @internal (undocumented)
    protected readonly _defaultContext?: TC;
    get isOptional(): boolean;
    // @internal (undocumented)
    protected _isOptional: boolean;
    map<T2>(mapper: (from: T) => Result<T2>): Converter<T2, TC>;
    mapConvert<T2>(mapConverter: Converter<T2>): Converter<T2, TC>;
    mapConvertItems<TI>(mapConverter: Converter<TI, unknown>): Converter<TI[], TC>;
    mapItems<TI>(mapper: (from: unknown) => Result<TI>): Converter<TI[], TC>;
    optional(onError?: OnError): Converter<T | undefined, TC>;
    // @internal (undocumented)
    protected _traits(traits?: Partial<ConverterTraits>): ConverterTraits;
    // @internal (undocumented)
    protected _with(traits: Partial<ConverterTraits>): this;
    withBrand<B extends string>(brand: B): Converter<Brand<T, B>, TC>;
    withConstraint(constraint: (val: T) => boolean | Result<T>, options?: ConstraintOptions): Converter<T, TC>;
    withItemTypeGuard<TI>(guard: (from: unknown) => from is TI, message?: string): Converter<TI[], TC>;
    withTypeGuard<TI>(guard: (from: unknown) => from is TI, message?: string): Converter<TI, TC>;
}

// @public
const boolean: BaseConverter<boolean, undefined>;

// @public
const boolean_2: BooleanValidator<unknown>;

// @public
class BooleanValidator<TC = unknown> extends GenericValidator<boolean, TC> {
    constructor(params?: BooleanValidatorConstructorParams<TC>);
    static validateBoolean(from: unknown): boolean | Failure<boolean>;
}

// @public
type BooleanValidatorConstructorParams<TC = unknown> = GenericValidatorConstructorParams<boolean, TC>;

// @public
export type Brand<T, B> = T & {
    __brand: B;
};

// @public
export function captureResult<T>(func: () => T): Result<T>;

declare namespace Classes {
    export {
        StringValidator,
        StringValidatorConstructorParams,
        BooleanValidator,
        BooleanValidatorConstructorParams,
        NumberValidator,
        NumberValidatorConstructorParams,
        FieldValidators,
        ObjectValidator,
        ObjectValidatorConstructorParams,
        ObjectValidatorOptions
    }
}

// @public
function computeHash(parts: string[]): string;

// @public
type Constraint<T> = (val: T) => boolean | Failure<T>;

// @public
export interface ConstraintOptions {
    readonly description: string;
}

// @public
type ConstraintTrait = FunctionConstraintTrait;

// Warning: (ae-internal-missing-underscore) The name "ConvertedToType" should be prefixed with an underscore because the declaration is marked as @internal
//
// @internal @deprecated
export type ConvertedToType<TCONV> = Infer<TCONV>;

// @public
export interface Converter<T, TC = undefined> extends ConverterTraits {
    readonly brand?: string;
    convert(from: unknown, context?: TC): Result<T>;
    convertOptional(from: unknown, context?: TC, onError?: OnError): Result<T | undefined>;
    readonly isOptional: boolean;
    map<T2>(mapper: (from: T) => Result<T2>): Converter<T2, TC>;
    mapConvert<T2>(mapConverter: Converter<T2>): Converter<T2, TC>;
    mapConvertItems<TI>(mapConverter: Converter<TI, unknown>): Converter<TI[], TC>;
    mapItems<TI>(mapper: (from: unknown) => Result<TI>): Converter<TI[], TC>;
    optional(onError?: OnError): Converter<T | undefined, TC>;
    withBrand<B extends string>(brand: B): Converter<Brand<T, B>, TC>;
    withConstraint(constraint: (val: T) => boolean | Result<T>, options?: ConstraintOptions): Converter<T, TC>;
    withItemTypeGuard<TI>(guard: (from: unknown) => from is TI, message?: string): Converter<TI[], TC>;
    withTypeGuard<TI>(guard: (from: unknown) => from is TI, message?: string): Converter<TI, TC>;
}

declare namespace Converters {
    export {
        templateString,
        enumeratedValue,
        mappedEnumeratedValue,
        literal,
        delimitedString,
        oneOf,
        arrayOf,
        extendedArrayOf,
        recordOf,
        mapOf,
        validateWith,
        element,
        optionalElement,
        field,
        optionalField,
        object,
        strictObject,
        discriminatedObject,
        transform,
        rangeTypeOf,
        rangeOf,
        StringMatchOptions,
        StringConverter,
        string,
        value,
        number,
        boolean,
        optionalString,
        isoDate,
        optionalNumber,
        optionalBoolean,
        stringArray,
        numberArray,
        KeyedConverterOptions,
        ObjectConverterOptions,
        FieldConverters,
        ObjectConverter,
        StrictObjectConverterOptions,
        DiscriminatedObjectConverters
    }
}
export { Converters }

// @public
export interface ConverterTraits {
    // (undocumented)
    readonly brand?: string;
    // (undocumented)
    readonly isOptional: boolean;
}

declare namespace Csv {
    export {
        readCsvFileSync
    }
}
export { Csv }

// @public
export const DEFAULT_RANGEOF_FORMATS: {
    minOnly: string;
    maxOnly: string;
    minMax: string;
};

// @public
const defaultValidatorTraits: ValidatorTraitValues;

// @public
function delimitedString(delimiter: string, options?: 'filtered' | 'all'): Converter<string[], string>;

// @public
export class DetailedFailure<T, TD> extends Failure<T> {
    constructor(message: string, detail: TD);
    get detail(): TD;
    // @internal (undocumented)
    protected _detail: TD;
    isFailure(): this is DetailedFailure<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "onFailure" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    onFailure(cb: DetailedFailureContinuation<T, TD>): DetailedResult<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "onSuccess" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    onSuccess<TN>(_cb: DetailedSuccessContinuation<T, TD, TN>): DetailedResult<TN, TD>;
}

// Warning: (ae-incompatible-release-tags) The symbol "DetailedFailureContinuation" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
//
// @public
export type DetailedFailureContinuation<T, TD> = (message: string, detail: TD) => DetailedResult<T, TD>;

// @beta
export type DetailedResult<T, TD> = DetailedSuccess<T, TD> | DetailedFailure<T, TD>;

// @public
export class DetailedSuccess<T, TD> extends Success<T> {
    constructor(value: T, detail?: TD);
    get detail(): TD | undefined;
    // @internal (undocumented)
    protected _detail?: TD;
    isSuccess(): this is DetailedSuccess<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "onFailure" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    onFailure(_cb: DetailedFailureContinuation<T, TD>): DetailedResult<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "onSuccess" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    onSuccess<TN>(cb: DetailedSuccessContinuation<T, TD, TN>): DetailedResult<TN, TD>;
}

// Warning: (ae-incompatible-release-tags) The symbol "DetailedSuccessContinuation" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
//
// @public
export type DetailedSuccessContinuation<T, TD, TN> = (value: T, detail?: TD) => DetailedResult<TN, TD>;

// @public
function discriminatedObject<T, TD extends string = string, TC = unknown>(discriminatorProp: string, converters: DiscriminatedObjectConverters<T, TD>): Converter<T, TC>;

// @public
type DiscriminatedObjectConverters<T, TD extends string = string, TC = unknown> = Record<TD, Converter<T, TC>>;

// @public
function element<T, TC = undefined>(index: number, converter: Converter<T, TC>): Converter<T, TC>;

// @public
function enumeratedValue<T>(values: T[]): Converter<T, T[]>;

// @beta
export class ExtendedArray<T> extends Array<T> {
    constructor(itemDescription: string, ...items: T[]);
    all(): T[];
    atLeastOne(failMessage?: string): Result<T[]>;
    first(failMessage?: string): Result<T>;
    static isExtendedArray<T>(a?: T[]): a is ExtendedArray<T>;
    // (undocumented)
    readonly itemDescription: string;
    single(predicate?: (item: T) => boolean): Result<T>;
}

// @beta
function extendedArrayOf<T, TC = undefined>(label: string, converter: Converter<T, TC>, onError?: OnError_2): Converter<ExtendedArray<T>, TC>;

// @public
function fail_2<T>(message: string): Failure<T>;
export { fail_2 as fail }

// @public
export class Failure<T> implements IResult<T> {
    constructor(message: string);
    getValueOrDefault(dflt?: T): T | undefined;
    getValueOrThrow(logger?: IResultLogger): never;
    isFailure(): this is Failure<T>;
    isSuccess(): this is Success<T>;
    get message(): string;
    onFailure(cb: FailureContinuation<T>): Result<T>;
    onSuccess<TN>(_: SuccessContinuation<T, TN>): Result<TN>;
    readonly success = false;
    toString(): string;
    // Warning: (ae-incompatible-release-tags) The symbol "withDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    withDetail<TD>(detail: TD, _successDetail?: TD): DetailedResult<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "withFailureDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    withFailureDetail<TD>(detail: TD): DetailedResult<T, TD>;
}

// @public
export type FailureContinuation<T> = (message: string) => Result<T>;

// @public
export function failWithDetail<T, TD>(message: string, detail: TD): DetailedFailure<T, TD>;

// @public
function field<T, TC = undefined>(name: string, converter: Converter<T, TC>): Converter<T, TC>;

// @public
type FieldConverters<T, TC = unknown> = {
    [key in keyof T]: Converter<T[key], TC>;
};

// @public
export type FieldInitializers<T> = {
    [key in keyof T]: (state: Partial<T>) => Result<T[key]>;
};

// @public
type FieldValidators<T, TC = unknown> = {
    [key in keyof T]: Validator<T[key], TC>;
};

// @beta
export function formatList<T>(format: string, items: T[], itemFormatter: Formatter<T>): Result<string>;

// @beta
export interface Formattable {
    format(format: string): Result<string>;
}

// @beta
export class FormattableBase {
    format(template: string): Result<string>;
    // @internal
    protected static _tryAddDetail(details: string[], label: string, value: string | undefined): void;
}

// @beta
export type FormatTargets = 'text' | 'markdown' | 'embed';

// @beta
export type Formatter<T> = (format: string, item: T) => Result<string>;

// @beta
export type FormattersByExtendedTarget<TFT extends FormatTargets, T> = Record<TFT, Formatter<T>>;

// @beta
export type FormattersByTarget<T> = FormattersByExtendedTarget<FormatTargets, T>;

// @public
interface FunctionConstraintTrait {
    // (undocumented)
    type: 'function';
}

// @public
class GenericValidator<T, TC = undefined> implements Validator<T, TC> {
    constructor(params: Partial<GenericValidatorConstructorParams<T, TC>>);
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    get brand(): string | undefined;
    // @internal
    protected _context(explicitContext?: TC): TC | undefined;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    guard(from: unknown, context?: TC): from is T;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    get isOptional(): boolean;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    optional(): Validator<T | undefined, TC>;
    // @internal (undocumented)
    protected readonly _options: ValidatorOptions<TC>;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    readonly traits: ValidatorTraits;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    validate(from: unknown, context?: TC): Result<T>;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    validateOptional(from: unknown, context?: TC): Result<T | undefined>;
    // @internal (undocumented)
    protected readonly _validator: ValidatorFunc<T, TC>;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    withBrand<B extends string>(brand: B): Validator<Brand<T, B>, TC>;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    withConstraint(constraint: Constraint<T>, trait?: ConstraintTrait): Validator<T, TC>;
}

// @public
interface GenericValidatorConstructorParams<T, TC> {
    // (undocumented)
    options?: ValidatorOptions<TC>;
    // (undocumented)
    traits?: Partial<ValidatorTraits>;
    // (undocumented)
    validator?: ValidatorFunc<T, TC>;
}

// @public
export function getTypeOfProperty<T extends object>(key: string | number | symbol, item: T): 'string' | 'number' | 'bigint' | 'boolean' | 'symbol' | 'undefined' | 'undefined' | 'object' | 'function' | undefined;

// @public
export function getValueOfPropertyOrDefault<T extends object>(key: string | number | symbol, item: T, defaultValue?: unknown): unknown | undefined;

declare namespace Hash {
    export {
        computeHash,
        Normalizer
    }
}
export { Hash }

// Warning: (ae-forgotten-export) The symbol "InnerInferredType" needs to be exported by the entry point index.d.ts
//
// @beta
export type Infer<TCONV> = TCONV extends Converter<infer TTO> ? InnerInferredType<TTO> : never;

// @public
export interface IResult<T> {
    getValueOrDefault(dflt?: T): T | undefined;
    getValueOrThrow(logger?: IResultLogger): T;
    isFailure(): this is Failure<T>;
    isSuccess(): this is Success<T>;
    onFailure(cb: FailureContinuation<T>): Result<T>;
    onSuccess<TN>(cb: SuccessContinuation<T, TN>): Result<TN>;
    readonly success: boolean;
    // Warning: (ae-incompatible-release-tags) The symbol "withDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    withDetail<TD>(detail: TD, successDetail?: TD): DetailedResult<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "withFailureDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    withFailureDetail<TD>(detail: TD): DetailedResult<T, TD>;
}

// @public
export interface IResultLogger {
    error(message: string): void;
}

// @public
export function isKeyOf<T extends object>(key: string | number | symbol, item: T): key is keyof T;

// @public
const isoDate: BaseConverter<Date, undefined>;

// @public
interface KeyedConverterOptions<T extends string = string, TC = undefined> {
    keyConverter?: Converter<T, TC>;
    onError?: 'fail' | 'ignore';
}

// @public
function literal<T>(value: T): Converter<T, unknown>;

// Warning: (ae-incompatible-release-tags) The symbol "mapDetailedResults" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
//
// @public
export function mapDetailedResults<T, TD>(results: Iterable<DetailedResult<T, TD>>, ignore: TD[]): Result<T[]>;

// @public
export function mapFailures<T>(results: Iterable<Result<T>>): string[];

// @public
function mapOf<T, TC = undefined, TK extends string = string>(converter: Converter<T, TC>): Converter<Map<TK, T>, TC>;

// @public
function mapOf<T, TC = undefined, TK extends string = string>(converter: Converter<T, TC>, onError: 'fail' | 'ignore'): Converter<Map<TK, T>, TC>;

// @public
function mapOf<T, TC = undefined, TK extends string = string>(converter: Converter<T, TC>, options: KeyedConverterOptions<TK, TC>): Converter<Map<TK, T>, TC>;

// @public
function mappedEnumeratedValue<T>(map: [T, unknown[]][], message?: string): Converter<T, undefined>;

// @public
export function mapResults<T>(results: Iterable<Result<T>>): Result<T[]>;

// @public
export function mapSuccess<T>(results: Iterable<Result<T>>): Result<T[]>;

// Warning: (ae-forgotten-export) The symbol "KeyedThingFactory" needs to be exported by the entry point index.d.ts
//
// @public
export function mapToRecord<TS, TD, TK extends string = string>(src: Map<TK, TS>, factory: KeyedThingFactory<TS, TD, TK>): Result<Record<TK, TD>>;

// @public
class Normalizer {
    // @internal
    protected _compareKeys(k1: unknown, k2: unknown): number;
    computeHash(from: unknown): Result<string>;
    // @internal
    protected _normalizeEntries(entries: Iterable<[unknown, unknown]>): [unknown, unknown][];
    // @internal
    protected _normalizeLiteral(from: string | number | bigint | boolean | symbol | undefined | Date | RegExp | null): Result<string>;
}

// @public
const number: BaseConverter<number, undefined>;

// @public
const number_2: NumberValidator<number, unknown>;

// @public
const numberArray: Converter<number[], undefined>;

// @public
class NumberValidator<T extends number = number, TC = unknown> extends GenericValidator<T, TC> {
    constructor(params?: NumberValidatorConstructorParams<T, TC>);
    static validateNumber<T extends number>(from: unknown): boolean | Failure<T>;
}

// @public
type NumberValidatorConstructorParams<T extends number = number, TC = unknown> = GenericValidatorConstructorParams<T, TC>;

// @public
function object<T>(properties: FieldConverters<T>, options?: ObjectConverterOptions<T>): ObjectConverter<T>;

// @public @deprecated
function object<T>(properties: FieldConverters<T>, optional: (keyof T)[]): ObjectConverter<T>;

// @public
function object_2<T, TC>(fields: FieldValidators<T, TC>, params?: Omit<ObjectValidatorConstructorParams<T, TC>, 'fields'>): ObjectValidator<T, TC>;

// @public
class ObjectConverter<T, TC = unknown> extends BaseConverter<T, TC> {
    constructor(fields: FieldConverters<T, TC>, options?: ObjectConverterOptions<T>);
    constructor(fields: FieldConverters<T, TC>, optional?: (keyof T)[]);
    addPartial(addOptionalProperties: (keyof T)[]): ObjectConverter<Partial<T>, TC>;
    readonly fields: FieldConverters<T>;
    readonly options: ObjectConverterOptions<T>;
    partial(options: ObjectConverterOptions<T>): ObjectConverter<Partial<T>, TC>;
    partial(optional?: (keyof T)[]): ObjectConverter<Partial<T>, TC>;
}

// @public
interface ObjectConverterOptions<T> {
    optionalFields?: (keyof T)[];
    strict?: boolean;
}

// Warning: (ae-forgotten-export) The symbol "ValidatorBase" needs to be exported by the entry point index.d.ts
//
// @public
class ObjectValidator<T, TC = unknown> extends ValidatorBase<T, TC> {
    constructor(params: ObjectValidatorConstructorParams<T, TC>);
    addPartial(addOptionalFields: (keyof T)[]): ObjectValidator<Partial<T>, TC>;
    // @internal (undocumented)
    protected readonly _allowedFields?: Set<keyof T>;
    readonly fields: FieldValidators<T>;
    // @internal (undocumented)
    protected readonly _innerValidators: FieldValidators<T>;
    readonly options: ObjectValidatorOptions<T, TC>;
    partial(options?: ObjectValidatorOptions<T, TC>): ObjectValidator<Partial<T>, TC>;
    // @internal
    protected static _resolveValidators<T, TC>(fields: FieldValidators<T, TC>, options?: ObjectValidatorOptions<T, TC>): FieldValidators<T, TC>;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // @internal (undocumented)
    protected _validate(from: unknown, context?: TC): boolean | Failure<T>;
}

// Warning: (ae-forgotten-export) The symbol "ValidatorBaseConstructorParams" needs to be exported by the entry point index.d.ts
//
// @public
interface ObjectValidatorConstructorParams<T, TC> extends ValidatorBaseConstructorParams<T, TC> {
    fields: FieldValidators<T>;
    options?: ObjectValidatorOptions<T, TC>;
}

// @public
interface ObjectValidatorOptions<T, TC> extends ValidatorOptions<TC> {
    optionalFields?: (keyof T)[];
    strict?: boolean;
}

// @public
function oneOf<T, TC = unknown>(converters: Array<Converter<T, TC>>, onError?: OnError_2): Converter<T, TC>;

// @public
const optionalBoolean: Converter<boolean | undefined, undefined>;

// @public
function optionalElement<T, TC = undefined>(index: number, converter: Converter<T, TC>): Converter<T | undefined, TC>;

// @public
function optionalField<T, TC = undefined>(name: string, converter: Converter<T, TC>): Converter<T | undefined, TC>;

// @public
export function optionalMapToPossiblyEmptyRecord<TS, TD, TK extends string = string>(src: Map<TK, TS> | undefined, factory: KeyedThingFactory<TS, TD, TK>): Result<Record<TK, TD>>;

// @public
export function optionalMapToRecord<TS, TD, TK extends string = string>(src: Map<TK, TS> | undefined, factory: KeyedThingFactory<TS, TD, TK>): Result<Record<TK, TD> | undefined>;

// @public
const optionalNumber: Converter<number | undefined, undefined>;

// @public
export function optionalRecordToMap<TS, TD, TK extends string = string>(src: Record<TK, TS> | undefined, factory: KeyedThingFactory<TS, TD, TK>): Result<Map<TK, TD> | undefined>;

// @public
export function optionalRecordToPossiblyEmptyMap<TS, TD, TK extends string = string>(src: Record<TK, TS> | undefined, factory: KeyedThingFactory<TS, TD, TK>): Result<Map<TK, TD>>;

// @public
const optionalString: Converter<string | undefined, unknown>;

// @public
export function populateObject<T>(initializers: FieldInitializers<T>, order?: (keyof T)[]): Result<T>;

// Warning: (ae-incompatible-release-tags) The symbol "propagateWithDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
//
// @public
export function propagateWithDetail<T, TD>(result: Result<T>, detail: TD, successDetail?: TD): DetailedResult<T, TD>;

// @public
export class RangeOf<T> implements RangeOfProperties<T> {
    constructor(min?: T, max?: T);
    check(t: T): 'less' | 'included' | 'greater';
    // @internal
    protected _compare(t1: T, t2: T): 'less' | 'equal' | 'greater';
    static createRange<T>(init?: RangeOfProperties<T>): Result<RangeOf<T>>;
    // @internal
    protected static _defaultCompare<T>(t1: T, t2: T): 'less' | 'equal' | 'greater';
    findTransition(t: T): T | undefined;
    format(format: (value: T) => string | undefined, formats?: RangeOfFormats): string | undefined;
    includes(t: T): boolean;
    readonly max?: T;
    readonly min?: T;
    static propertiesToString<T>(range: RangeOfProperties<T>, formats?: RangeOfFormats, emptyValue?: T): string | undefined;
    toFormattedProperties(format: (value: T) => string | undefined): RangeOfProperties<string>;
}

// @public
function rangeOf<T, TC = unknown>(converter: Converter<T, TC>): Converter<RangeOf<T>, TC>;

// @public
export interface RangeOfFormats {
    // (undocumented)
    maxOnly: string;
    // (undocumented)
    minMax: string;
    // (undocumented)
    minOnly: string;
}

// @public
export interface RangeOfProperties<T> {
    // (undocumented)
    readonly max?: T;
    // (undocumented)
    readonly min?: T;
}

// @public
function rangeTypeOf<T, RT extends RangeOf<T>, TC = unknown>(converter: Converter<T, TC>, constructor: (init: RangeOfProperties<T>) => Result<RT>): Converter<RT, TC>;

// @beta
function readCsvFileSync(srcPath: string): Result<unknown>;

// @public
function recordOf<T, TC = undefined, TK extends string = string>(converter: Converter<T, TC>): Converter<Record<TK, T>, TC>;

// @public
function recordOf<T, TC = undefined, TK extends string = string>(converter: Converter<T, TC>, onError: 'fail' | 'ignore'): Converter<Record<TK, T>, TC>;

// @public
function recordOf<T, TC = undefined, TK extends string = string>(converter: Converter<T, TC>, options: KeyedConverterOptions<TK, TC>): Converter<Record<TK, T>, TC>;

// @public
export function recordToMap<TS, TD, TK extends string = string>(src: Record<TK, TS>, factory: KeyedThingFactory<TS, TD, TK>): Result<Map<TK, TD>>;

// @public
export type Result<T> = Success<T> | Failure<T>;

// @beta
export type ResultDetailType<T> = T extends DetailedResult<unknown, infer TD> ? TD : never;

// @beta
export type ResultValueType<T> = T extends Result<infer TV> ? TV : never;

// @public
function strictObject<T>(properties: FieldConverters<T>, options?: StrictObjectConverterOptions<T>): ObjectConverter<T>;

// @public @deprecated
function strictObject<T>(properties: FieldConverters<T>, optional: (keyof T)[]): ObjectConverter<T>;

// @public
type StrictObjectConverterOptions<T> = Omit<ObjectConverterOptions<T>, 'strict'>;

// @public
const string: StringConverter<string, unknown>;

// @public
const string_2: StringValidator<string, unknown>;

// @public
const stringArray: Converter<string[], unknown>;

// @public
class StringConverter<T extends string = string, TC = unknown> extends BaseConverter<T, TC> {
    constructor(defaultContext?: TC, traits?: ConverterTraits, converter?: (from: unknown, self: Converter<T, TC>, context?: TC) => Result<T>);
    // @internal (undocumented)
    protected static _convert<T extends string>(from: unknown): Result<T>;
    matching(match: string, options?: Partial<StringMatchOptions>): StringConverter<T, TC>;
    matching(match: string[], options?: Partial<StringMatchOptions>): StringConverter<T, TC>;
    matching(match: Set<T>, options?: Partial<StringMatchOptions>): StringConverter<T, TC>;
    matching(match: RegExp, options?: Partial<StringMatchOptions>): StringConverter<T, TC>;
    // @internal (undocumented)
    protected static _wrap<T extends string, TC>(wrapped: StringConverter<T, TC>, converter: (from: T) => Result<T>, traits?: ConverterTraits): StringConverter<T, TC>;
}

// @public
interface StringMatchOptions {
    message?: string;
}

// @public
class StringValidator<T extends string = string, TC = unknown> extends GenericValidator<T, TC> {
    constructor(params?: StringValidatorConstructorParams<T, TC>);
    static validateString<T extends string>(from: unknown): boolean | Failure<T>;
}

// @public
type StringValidatorConstructorParams<T extends string = string, TC = unknown> = GenericValidatorConstructorParams<T, TC>;

// @public
export function succeed<T>(value: T): Success<T>;

// @public
export function succeedWithDetail<T, TD>(value: T, detail?: TD): DetailedSuccess<T, TD>;

// @public
export class Success<T> implements IResult<T> {
    constructor(value: T);
    getValueOrDefault(dflt?: T): T | undefined;
    getValueOrThrow(_logger?: IResultLogger): T;
    isFailure(): this is Failure<T>;
    isSuccess(): this is Success<T>;
    onFailure(_: FailureContinuation<T>): Result<T>;
    onSuccess<TN>(cb: SuccessContinuation<T, TN>): Result<TN>;
    readonly success = true;
    get value(): T;
    // Warning: (ae-incompatible-release-tags) The symbol "withDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    withDetail<TD>(detail: TD, successDetail?: TD): DetailedResult<T, TD>;
    // Warning: (ae-incompatible-release-tags) The symbol "withFailureDetail" is marked as @public, but its signature references "DetailedResult" which is marked as @beta
    withFailureDetail<TD>(_detail: TD): DetailedResult<T, TD>;
}

// @public
export type SuccessContinuation<T, TN> = (value: T) => Result<TN>;

// @public
function templateString(defaultContext?: unknown): StringConverter<string, unknown>;

// @public
function transform<T, TC = unknown>(properties: FieldConverters<T, TC>): Converter<T, TC>;

// @public
function validateWith<T, TC = undefined>(validator: (from: unknown) => from is T, description?: string): Converter<T, TC>;

declare namespace Validation {
    export {
        Base,
        Classes,
        Validators,
        FunctionConstraintTrait,
        ConstraintTrait,
        ValidatorTraitValues,
        defaultValidatorTraits,
        ValidatorTraits,
        ValidatorOptions,
        Constraint,
        Validator
    }
}
export { Validation }

// @public
interface Validator<T, TC = undefined> {
    readonly brand: string | undefined;
    guard(from: unknown, context?: TC): from is T;
    readonly isOptional: boolean;
    optional(): Validator<T | undefined, TC>;
    readonly traits: ValidatorTraits;
    validate(from: unknown, context?: TC): Result<T>;
    validateOptional(from: unknown, context?: TC): Result<T | undefined>;
    withBrand<B extends string>(brand: B): Validator<Brand<T, B>, TC>;
    withConstraint(constraint: Constraint<T>, trait?: ConstraintTrait): Validator<T, TC>;
}

// @public
type ValidatorFunc<T, TC> = (from: unknown, context?: TC) => boolean | Failure<T>;

// @public
interface ValidatorOptions<TC> {
    // (undocumented)
    defaultContext?: TC;
}

declare namespace Validators {
    export {
        object_2 as object,
        string_2 as string,
        number_2 as number,
        boolean_2 as boolean
    }
}

// @public
class ValidatorTraits implements ValidatorTraitValues {
    constructor(init?: Partial<ValidatorTraitValues>, base?: ValidatorTraitValues);
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    readonly brand?: string;
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    readonly constraints: ConstraintTrait[];
    // Warning: (ae-unresolved-inheritdoc-reference) The @inheritDoc reference could not be resolved: This type of declaration is not supported yet by the resolver
    //
    // (undocumented)
    readonly isOptional: boolean;
}

// @public
interface ValidatorTraitValues {
    readonly brand?: string;
    readonly constraints: ConstraintTrait[];
    readonly isOptional: boolean;
}

// @internal @deprecated
const value: typeof literal;

// (No @packageDocumentation comment for this package)

```