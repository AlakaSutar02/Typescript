### What is TypeScript and why should you use it?

TypeScript is a statically typed superset of JavaScript that compiles to plain JavaScript. It adds optional type annotations, interfaces, generics, and advanced type features that catch errors at compile time rather than runtime. Teams use it to improve code maintainability, enable better IDE tooling, and make large codebases easier to refactor safely.

### What is the difference between type and interface in TypeScript?

Both type aliases and interfaces can describe object shapes, but they have key differences. Interfaces support declaration merging (multiple declarations merge into one) and are generally preferred for defining object shapes and class contracts. Type aliases are more flexible — they can represent primitives, unions, intersections, tuples, and mapped types. In most cases, prefer interface for objects and type for everything else.

### What are TypeScript generics and when do you use them?

Generics are type variables that let you write reusable code that works with multiple types while maintaining type safety. You use them when a function or class should operate on different types but the types are related (e.g., a function that returns the same type it receives). Without generics you'd have to use any and lose type safety.

### What is the difference between any, unknown, and never in TypeScript?

any disables type checking entirely — you can assign anything to it and do anything with it. unknown is the safe alternative — you can assign anything to it but must narrow the type before using it. never represents a type that can never occur — used as the return type of functions that always throw or never return, and appears in exhaustive checks.

### What are TypeScript utility types?

Utility types are built-in generic types that transform existing types. Common ones: Partial<T> makes all properties optional, Required<T> makes all required, Readonly<T> prevents mutations, Pick<T, K> selects a subset of keys, Omit<T, K> removes keys, Record<K, V> creates an object type, ReturnType<F> extracts a function's return type, and Awaited<T> unwraps a Promise type.

### What is type narrowing in TypeScript?

Type narrowing is the process of refining a broad type to a more specific one within a conditional block. TypeScript recognizes typeof, instanceof, in operator checks, equality checks, and truthiness checks as narrowing constructs. You can also write custom type guard functions using the 'is' syntax (value is Type) to narrow types in reusable ways.

### What is the any type and why is it dangerous?

any opts a variable out of type checking completely. It disables autocomplete, silences errors, and removes all benefits of TypeScript. Use unknown instead — it forces you to narrow the type before using the value.

### What is the difference between any and unknown?

unknown is the type-safe alternative to any. You can assign anything to unknown, but you cannot use it without first narrowing it (typeof, instanceof, a type guard). any bypasses all checks entirely.

### What is a union type?

A union type (A | B) means a value can be one of the listed types. TypeScript narrows unions through type guards, discriminated unions, or control flow analysis.

### What is an intersection type?

An intersection type (A & B) combines multiple types into one — the result must satisfy all of them. Commonly used to merge interfaces or mix in behaviours.
