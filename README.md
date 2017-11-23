# student-lang

The Student Programming Language

```
sum(n) =
 s = 0
 for i in n
   s += 1
   
O(sum(n)) = n
  by for i in n
    by +
    by =

built-in {
  reduce(f, n) =
    acc = 0
    for r in n
      acc = f(acc, r)
}

sum = reduce(+, n)
  by s = 0 == acc = 0
  by for i in n == for r in n
    by s += 1 == acc = f(acc, r)
      by + == f

cross(n) =
  c = 0
  for i in n
    for j in reverse n
      c += i * j

O(cross(n)) = n ^ 2
  by c = 0
  by for i in n 
    by for j in reverse n
      by c += i * j
        by i * j
        by +
        by =
        
built-in {
  zip(o, n, m) =
    z = []
    for zn in n
      for zm in m
        z += [o(zn, zm)]
}

cross(n) = reduce(+, zip(*, n, reverse n))
  by for z in n
```

# Design Goals

- Educational Language
- Inspired by C0, TLA+/PlusCal/TLAPS, and Isabelle/HOL
- Integers only
- Cost semantics with proofs
- Correctness properties with proofs
- Command-line/Compiler driven

# Implementation

- OCaml
