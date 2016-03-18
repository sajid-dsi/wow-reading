# Algorithm Cheatsheet

This cheatsheet is prepared as part of my exam for CIS775 (Algorithm Analysis)

  Kruskal's Algorithm
  check [this] (http://www.personal.kent.edu/~rmuhamma/Algorithms/MyAlgorithms/GraphAlgor/kruskalAlgor.htm)

  _Generic loop invariant : Prior to each iteration, A is a subset of some minimum spanning tree._

    KRUSKAL(V, E, w)

    A ← { }          ▷ Set A will ultimately contains the edges of the MST
    for each vertex v in V
         do MAKE-SET(v)
    sort E into nondecreasing order by weight w
    for each (u, v) taken from the sorted list
      do if FIND-SET(u) != FIND-SET(v) then
          A ← A ∪ {(u, v)}
          UNION(u, v)
    return A

**Runtime:** *O(ElogV)*
