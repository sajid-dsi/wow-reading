# Algorithm Cheatsheet

This cheatsheet is prepared as part of my exam for CIS775 (Algorithm Analysis)

  Kruskal's Algorithm
  check [this] (http://www.personal.kent.edu/~rmuhamma/Algorithms/MyAlgorithms/GraphAlgor/kruskalAlgor.htm)

  _generic loop invariant :_ *Prior to each iteration, A is a subset of some minimum spanning tree.*
    KRUSKAL(V, E, w)
    ```
    **A ← { }**           ▷ Set A will ultimately contains the edges of the MST
    for each vertex v in V
         do **MAKE-SET(v)**
    sort _E_ into nondecreasing order by weight w
    for each *(u, v)* taken from the sorted list
      do if **FIND-SET(u)** != **FIND-SET(v)** then
          _A ← A ∪ {(u, v)}_
          *UNION(u, v)*
    return _A_
```
**Runtime:** *O(ElogV)*
