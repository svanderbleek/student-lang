# student-lang

The Student Programming Language

```
set_cost(<, 1)

f n =
 for e in 1 .. n
   e < 3
   
prove cost(f), param(f, n) by
  cost(for, n) * cost(<)
```

# Design Goals

- Educational Language
- Inspired by C0, TLA+/PlusCal/TLAPS, and Isabelle/HOL
- Cost semantics with proofs
- Correctness properties with proofs
- Command-line/Compiler driven

# Implementation

- OCaml is a strong choice
