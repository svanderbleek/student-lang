# student-lang

The Student Programming Language

```
@ x <= y
- midpoint x y in x..y
by x + a >= if a >= 0
by x + a >= x if a <= 0 and
by y-x/2 >= 0
by y+x/2 <= y if x <= y
- x + midpoint x y + midpoint x y = y or x + midpoint x y + 1 = y
by y-x/2 + y-x/2 = y - x
by x + -x = 0
! midpoint x y = 1 if +,/ = 1 by midpoint.L1
midpoint x y =
  x + y-x/2
```

# Design Goals

- Educational language
- Inspired by C0, TLA+/PlusCal/TLAPS, Isabelle/Isar
- Semantics:
  - `@` for assumptions, `-` for statement, `by` for proof, `!` for cost
  - implicit quantification in meta language
  - functions, integers, and integer arrays
- Cost semantics with proofs
- Correctness properties with proofs
- Command-line/compiler driven
