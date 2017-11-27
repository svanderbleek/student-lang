# student-lang

The Student Programming Language

```
| sum-of-two
| find a pair of two ints that sum to target

@xy-targ exists x, y in ints with x + y = targ
sum-of-two ints targ =
  @init
  store := []
  @for ints
  for int in ints
    @int store[int] => exists num in traversed ints with num = targ - int
    if store[int] return store[int], int
    @store store[int]
    increment-store: store[targ - int] := int

- +* sum-of-two ints int = int
by @xy-targ and @int

- time size = ints
by @for

- space size = ints
by @init and @store

| sum-of-two!
| partial function

sum-of-two! ints targ =
  handle sum-of-two ints targ return 0
```

# Goals

- educational language
- inspired by C0, TLA+/PlusCal/TLAPS, Isabelle/Isar, CalcCheck
- semantics:
  - `|` for comment, `@` for facts, `-` for statement, `by` for proof
  - specific to `@` language: `exists`, `=`, `with`, `=>`,`handle`
  - implicit quantification in meta language
  - functions, integers, and integer arrays
- cost semantics with proofs
- correctness properties with proofs
- command-line/compiler driven


# References

- http://calccheck.mcmaster.ca/
- https://en.wikipedia.org/wiki/Transdichotomous_model
- http://adam.chlipala.net/frap/

