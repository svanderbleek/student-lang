# student-lang

The Student Programming Language

```
sum n =
 sum = 0
 for i in n
   sum += 1
 sum
   
O(sum) = n
by for i in n
by +=

cross n =
  cross = 0
  for i in n
    for j in n
      cross += i * j

O(cross) = n ^ 2 
by for i in n 
  by for j in n
    by * /\ by +=
```

# Design Goals

- Educational Language
- Inspired by C0, TLA+/PlusCal/TLAPS, and Isabelle/HOL
- Integers only
- Cost semantics with proofs
- Correctness properties with proofs
- Command-line/Compiler driven

# Implementation

- OCaml is a strong choice
