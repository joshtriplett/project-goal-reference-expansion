r[concurrency]
# Concurrency

r[concurrency.intro]
Rust provides language and library features for writing [concurrent programs]. These features are designed to prevent data races --- situations in which multiple threads access the same memory without proper synchronization, with at least one of the accesses modifying that memory.

This chapter describes the traits, types, and concepts that Rust uses to express and enforce safe concurrency.

[concurrent programs]: glossary.md#concurrent-program
