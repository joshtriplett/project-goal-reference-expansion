r[concurrency]
# Concurrency

r[concurrency.intro]
Rust provides language and library features for writing [concurrent programs]. These features are designed to prevent [data races] --- situations in which multiple threads access the same memory without proper synchronization, with at least one of the accesses modifying that memory.

This chapter describes the traits, types, and concepts that Rust uses to express and enforce safe concurrency.

r[concurrency.send-and-sync]
## Send and Sync

r[concurrency.send-and-sync.intro]
The [`Send`] and [`Sync`] traits are [unsafe traits] used by the Rust type system to track which types can be safely used across thread boundaries.

These traits are marker traits with no methods. Implementing them asserts that a type has the intrinsic properties required for safe concurrent use. The compiler automatically implements these traits for most types when possible, but they can also be implemented manually. Providing an incorrect manual implementation can cause [undefined behavior].

[concurrent programs]: glossary.md#concurrent-program
[data races]: glossary.md#data-race
[`Send`]: special-types-and-traits.md#Send
[`Sync`]: special-types-and-traits.md#Sync
[unsafe traits]: items/traits.md#unsafe-traits
[undefined behavior]: glossary.md#undefined_behavior
