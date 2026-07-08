# NeetCode 150 — 21 Mindmaps (Hinglish, mermaid source)
Kisi bhi block ko https://mermaid.live me paste karke diagram dekho. Branch labels Hinglish me hain, technical terms English me.

---

## #1 Merge K Sorted Lists
```mermaid
mindmap
  root((Merge K Sorted Lists))
    Engine kaise solve karein
      Min-heap of k value, src, pos
      Divide and conquer pairwise
      Loser/tournament tree huge k
    Source ka type
      Linked lists / arrays
      Iterators you can't rewind
      Matrix rows / pair-space
      Generated streams
    Follow-ups interviewer aage kya puchega
      Streaming / infinite lists
      External merge exceeds RAM
      Distributed merge across nodes
      Backpressure and bounded queues
      Pause / resume / checkpoint
      Fault tolerance / re-merge on failure
    Correctness kahan galti hoti hai
      Total order with duplicates
      Preserve source order stable
      Multi-key / secondary sort
```

## #2 Sliding Window
```mermaid
mindmap
  root((Sliding Window))
    Window ka type
      Fixed size k
      Variable / longest
      Variable / shortest
      Exactly-k = atMost k - atMost k-1
    Window ke andar kya track karein
      Sum / product
      Freq hashmap
      Distinct count
      Monotonic deque max/min
    Follow-ups interviewer aage kya puchega
      Streaming / infinite input
      Thread-safe window P99 tracker
      Window over event-time not index
      Per-key / multiple windows
    Correctness kahan galti hoti hai
      Duplicates allowed?
      At-most vs exactly K
      Negative numbers break shrink
    Output kaisa chahiye
      Length / substring / count
```

## #3 Two Pointers
```mermaid
mindmap
  root((Two Pointers))
    Flavor type
      Converging L/R sorted
      Fast and slow cycle/mid
      Read / write in-place
      Partition Dutch flag
      Merge two sorted base of Merge-K
    Follow-ups interviewer aage kya puchega
      Array too big for RAM external
      Streaming no backward index
      k-sum generalization
      Duplicates skip logic
    Correctness kahan galti hoti hai
      In-place O 1 space
      Stability of equals
      Overflow on sum compares
    Milte-julte problems cousins
      Trapping rain water
      Container with most water
```

## #4 Prefix Sum + HashMap
```mermaid
mindmap
  root((Prefix Sum + HashMap))
    Dimension kis type ka
      1-D range sum
      2-D integral image
      Prefix XOR
      Prefix count / parity
    HashMap ka jugaad
      Sum==K → seen prefix-K
      Divisible by K → seen prefix mod K
      Longest vs count
    Follow-ups interviewer aage kya puchega
      Streaming running prefix
      Mutable → Fenwick/BIT Concept 20
      2-D region queries
      Negative numbers / large K
    Milte-julte problems cousins
      Range queries → segment tree
      Count of range sum merge sort
```

## #5 Monotonic Stack
```mermaid
mindmap
  root((Monotonic Stack))
    Variants types
      Next greater / smaller
      Previous greater / smaller
      Increasing vs decreasing
      Indices vs values
    Kahan use hota hai Applications
      Daily temperatures / spans
      Largest rectangle in histogram
      Trapping rain water stack form
      Remove-k-digits / smallest
      Basic calculator parens
    Follow-ups interviewer aage kya puchega
      Streaming stock spanner
      2-D maximal rectangle
      Circular next greater II
    Correctness kahan galti hoti hai
      Ties strict vs non-strict pop
      Operator precedence / nesting
```

## #6 Binary Search (value & answer-space)
```mermaid
mindmap
  root((Binary Search))
    Array par array me search
      Classic target
      Rotated sorted pivot
      First/last occurrence
      2-D matrix search
    Answer par search karo
      Min largest sum / capacity
      Koko eating rate
      Kth smallest in matrix
      Split array / allocate pages
    Follow-ups interviewer aage kya puchega
      Duplicates worst O n
      Unknown length galloping
      Parallel/bucketed first-bad
      Expensive predicate → min calls
    Correctness kahan galti hoti hai
      Overflow in mid
      Lower vs upper bound off-by-one
      Monotonic predicate proof
```

## #7 Trees & Graph Traversal (DFS / BFS / Multi-source)
```mermaid
mindmap
  root((DFS / BFS))
    Traversal ghumne ke tareeke
      DFS pre/in/post-order
      BFS level order
      Multi-source BFS
      Bidirectional BFS
    Grid par
      Islands / components
      Rotting oranges multi-source
      Walls and gates / nearest-exit
      Flood fill
    Subtree DP postorder me
      Height / diameter
      Path sum / max path
      Delete node → recompute height
    Follow-ups interviewer aage kya puchega
      Graph exceeds memory
      Weighted → Dijkstra Concept 16
      Cycle detect → topo Concept 8
      Serialize / deserialize
      Concurrent / streaming edges
```

## #8 Topological Sort (DAG ordering)
```mermaid
mindmap
  root((Topological Sort))
    Engine kaise solve karein
      Kahn BFS in-degree queue
      DFS postorder + colors
      Cycle detection 3-color
    Kahan use hota hai Applications
      Course schedule / prereqs
      Build systems / task deps
      Package/version resolution
      Spark job DAG scheduling
    Follow-ups interviewer aage kya puchega
      Report the cycle not just detect
      Parallel schedule min time + durations
      Weighted longest / critical path
      Lexicographically smallest order
      Streaming edges arrive over time
    Correctness kahan galti hoti hai
      Multiple valid orders
      Disconnected components
      Self-loops / dup edges
```

## #9 Union-Find (Disjoint Set Union)
```mermaid
mindmap
  root((Union-Find / DSU))
    Core operations main kaam
      find + path compression
      union by rank/size
      count components
    Kahan use hota hai Applications
      Redundant connection / undirected cycle
      Accounts merge / friend circles
      Number of provinces
      Kruskal MST edge selection
      Percolation / grid connectivity
    Follow-ups interviewer aage kya puchega
      Union w/ rollback offline
      Weighted DSU relations/ratios
      Dynamic edges over time
      Distributed / sharded components
    BFS/DFS se kab better
      DSU when edges stream / many queries
      BFS/DFS when one static traversal
```

## #10 Backtracking
```mermaid
mindmap
  root((Backtracking))
    Shape type
      Subsets / combinations
      Permutations
      Partition / split
      Grid placement N-queens, sudoku
    Pruning branches kaatna
      Sort + skip duplicates
      Feasibility bound branch and bound
      Constraint propagation
    Follow-ups interviewer aage kya puchega
      Count only vs enumerate all
      Kth solution don't build all
      Memoize overlapping → DP
      Iterative / explicit stack
    Correctness kahan galti hoti hai
      Duplicate elements
      Reuse allowed? combination sum
      Lexicographic order required
```

## #11 Dynamic Programming
```mermaid
mindmap
  root((Dynamic Programming))
    Family types
      1-D linear rob/decode/jump
      Knapsack 0-1, unbounded, coin
      2-D grid paths
      String DP LCS, edit distance
      Interval DP MCM, burst balloons
    Method kaise banayein
      Top-down memo
      Bottom-up table
      Rolling array space O 1
    Follow-ups interviewer aage kya puchega
      Reconstruct solution not just value
      Count ways vs optimize value
      Space optimize to 1-D
      Huge N → matrix expo / math
    Correctness kahan galti hoti hai
      Base cases / empty inputs
      Unbounded vs 0-1 loop order
      Negative weights / cycles
```

## #12 Intervals & Sweep Line
```mermaid
mindmap
  root((Intervals / Sweep))
    Operation kya karna hai
      Merge overlapping
      Insert into sorted set
      Count overlaps / min rooms
      Erase / non-overlapping max
    Engine kaise solve karein
      Sort by start, compare last
      Sweep events +1 / -1
      Min-heap of end times
    Follow-ups interviewer aage kya puchega
      Streaming intervals online
      Weighted intervals DP scheduling
      2-D intervals / rectangle area
      Calendar w/ k overlaps allowed
    Correctness kahan galti hoti hai
      Touch vs overlap 1,2 , 2,3
      Open vs closed endpoints
      Ties at same coordinate
```

## #13 Design / In-Memory Stores (LRU, TTL, iterators)
```mermaid
mindmap
  root((Design / In-Memory))
    Base builds kya banate hain
      LRU hashmap + DLL
      LFU freq buckets
      TTL cache expiry index
      In-memory KV w/ iterators
      Rate limiter token/sliding
      Memory allocator malloc/free
    Follow-ups interviewer aage kya puchega
      Make it thread-safe Concept 21
      TTL lazy vs active eviction
      Weighted / size-bounded eviction
      Snapshot / versioned reads
      Persistence / crash recovery
      Distributed / sharded + clock skew
    Correctness kahan galti hoti hai
      Eviction during iteration
      Race conditions double-checked lock
      Idempotent writes
```

## #14 Fast & Slow Pointers / Linked-List Surgery
```mermaid
mindmap
  root((Fast/Slow and List Surgery))
    Fast/slow pointers
      Floyd cycle detect + start
      Find middle
      Nth from end
      Happy number on values
    List surgery pointer todna-jodna
      Reverse iterative/recursive
      Reorder list
      Reverse in k-groups
      Merge two sorted base of Merge-K
      Copy list w/ random pointer
    Follow-ups interviewer aage kya puchega
      Doubly vs singly
      Concurrent modification
      Immutable / persistent list
      Streaming / unknown length
      Strict O 1 extra space
    Correctness kahan galti hoti hai
      Null / single-node handling
      Off-by-one on nth
      Even vs odd length middle
```

## #15 Trie (Prefix Tree)
```mermaid
mindmap
  root((Trie))
    Structure banawat
      children map/array
      isEnd marker
      count / rank at node
    Operations kya kar sakte ho
      insert / search / startsWith
      delete word
      DFS collect by prefix
    Kahan use hota hai Applications
      Autocomplete / typeahead
      Word Search II trie + grid DFS
      Longest-match tokenizer
      Replace words / dictionary
      Longest-prefix-match IP routing
      Maximum XOR binary trie
    Follow-ups interviewer aage kya puchega
      Streaming inserts
      Memory compress → radix/Patricia
      Ranked top-k autocomplete
      Unicode / case handling
    Correctness kahan galti hoti hai
      Shared prefixes / end markers
```

## #16 Dijkstra / Bellman-Ford / MST (weighted graphs)
```mermaid
mindmap
  root((Dijkstra / BF / MST))
    Shortest path chhota raasta
      Dijkstra PQ frontier
      Bellman-Ford negatives
      SPFA / Floyd-Warshall all pairs
      A* / bidirectional huge graph
    MST spanning tree
      Prim heap
      Kruskal sort + DSU
    Variants types
      Cheapest within k stops
      Path w/ max-min capacity
      Second shortest path
      Multiplicative weights
    Follow-ups interviewer aage kya puchega
      Negative edges → BF
      Dynamic / streaming edges
      Distributed / sharded graph
    Correctness kahan galti hoti hai
      Lazy deletion / revisit w/ heap
      Overflow, disconnected nodes
```

## #17 Bit Manipulation
```mermaid
mindmap
  root((Bit Manipulation))
    Core tricks jugaad
      XOR pairing a^a=0
      n and n-1 clears lowest set
      n and -n isolates lowest set
      shifts and masks
    Kahan use hota hai Applications
      Single number I/II/III
      Counting bits DP on bits
      Sum without + / -
      Subsets via bitmask
      Bitmask DP TSP / assignment
      Missing number / reverse bits
    Follow-ups interviewer aage kya puchega
      Fixed-width overflow 32/64
      Two's complement / negatives
      Bit-parallel / SIMD
      Big integers
    Correctness kahan galti hoti hai
      Signed vs logical shift
      Endianness / overflow
```

## #18 Math & Geometry
```mermaid
mindmap
  root((Math and Geometry))
    Number theory
      GCD / LCM
      Sieve of Eratosthenes
      Modular exponentiation
      Prime factorization
    Matrix
      Rotate in place
      Spiral order
      Set zeroes / transpose
    Fast math jaldi calculation
      Pow by squaring
      Sqrt via binary search / Newton
    Geometry
      Points on a line
      Convex hull / intersection / area
    Follow-ups interviewer aage kya puchega
      Overflow / bignum
      Modular arithmetic 1e9+7
      Float precision / epsilon
      Streaming numeric stats
```

## #19 Greedy (interval scheduling, Huffman)
```mermaid
mindmap
  root((Greedy))
    Common patterns
      Interval scheduling by end time
      Min arrows / min rooms
      Huffman merge heap
      Jump game reachability
      Gas station
      Task scheduler cooldown
      Partition labels
    Proof sahi kaise sabit karein
      Exchange argument
      Stays-ahead
    Follow-ups interviewer aage kya puchega
      Weighted → DP instead
      Tie-breaking rules
      Streaming greedy
      When greedy FAILS → counterexample
    Correctness kahan galti hoti hai
      Why greedy is valid
      Sort-key choice
```

## #20 Segment Tree / Fenwick (BIT) — the mutable-range escalation
```mermaid
mindmap
  root((Segment Tree / Fenwick))
    Structures banawat
      Fenwick/BIT prefix sum + point update
      Segment tree any associative op
      Lazy propagation range update
      Merge-sort tree
      2-D BIT
    Kahan use hota hai Applications
      Mutable range sum
      Range min / max
      Count of smaller after self
      Count of range sum
      Skyline / interval stabbing
    Follow-ups interviewer aage kya puchega
      Lazy prop for range assign
      Persistent tree historical queries
      Coordinate compression
      Distributed / sharded aggregates
    Correctness kahan galti hoti hai
      1-indexing BIT
      Lazy push-down order
      Overflow
```

## #21 Concurrency Primitives (cross-cutting: Anthropic / Netflix / Citadel)
```mermaid
mindmap
  root((Concurrency Primitives))
    Primitives basic tools
      Mutex / lock
      Read-write lock
      Atomic / CAS
      Condition variable
      Semaphore
      Lock striping / sharding
    Common patterns
      Producer-consumer bounded buffer
      Thread-safe cache / counter
      Double-checked locking
      Read-copy-update
      Futures / async
    Pitfalls kahan phasoge
      Deadlock / livelock
      Lost wakeups
      ABA problem
      False sharing / starvation
    Follow-ups interviewer aage kya puchega
      Lock-free via CAS
      Sharded locks for throughput
      Backpressure / bounded queues
      Clock skew distributed + idempotency
    Correctness kahan galti hoti hai
      Invariants under interleaving
      Memory visibility / happens-before
```
