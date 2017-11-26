# student-lang

The Student Programming Language

```
| sum-of-two

@ exist x, y in ints with x + y = targ

sum-of-two ints targ =
  store := {}
  for int in ints
    store[int]? -> [store[int], int]
    store[targ - int] := int

- sum of sum-of-two ints int = int
by for i in ints we store[targ - i] = i or -> 
by store[targ -  x] + store[targ - y] = targ
  by store[x + y - x] = store[y] = y
  by store[x + y - y] = store[x] = y

! size ints
by for i in ints

* size ints
by for i in ints we store[]
```

# Design Goals

- Educational language
- Inspired by C0, TLA+/PlusCal/TLAPS, Isabelle/Isar
- Semantics:
  - `|` for definition, `@` for assumptions, `-` for statement, `by` for proof, `!` for time cost, `*` for space cost
  - implicit quantification in meta language
  - functions, integers, and integer arrays
- Cost semantics with proofs
- Correctness properties with proofs
- Command-line/compiler driven
