### Type inference is TypeScript's ability to automatically determine a value's type without an explicit annotation.

Variable initialization — const x = 42 infers number

Function return type — inferred from the return expression

Default parameters — function greet(name = 'World') infers name: string

Destructuring — inferred from the source type

Generic instantiation — argument types drive the type parameter

### What is the difference between any, unknown, and never in TypeScript?

These three types occupy opposite ends of the type hierarchy.

any — the escape hatch. Disables all type checking for that value. Assignable to and from everything.
unknown — the type-safe alternative to any. You must narrow it before using it.
never — the bottom type. A value that can never exist.
Used for:
Functions that never return (throw or infinite loop)

    Exhaustive checks in switch/if statements

    Impossible intersections

### type vs interface :

Both define object shapes, but they have different capabilities:

Interface — designed for object/class shapes, supports declaration merging:
Type alias — more powerful, works with any type including primitives, unions, tuples, and mapped types:
