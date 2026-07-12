# LLD  — 12 Pattern Mindmaps 

---

## #1 OOP Modelling & SOLID (the foundation)
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((OOP Modelling and SOLID the foundation))
    Nouns to entities
      Entities / value objects
      Enums for states and types
      No god class, no Manager/Helper
    Verbs to services
      Service layer holds behaviour
      Each method does one thing
      models / services / strategies folders
    SOLID galti yahan hoti hai
      SRP - one reason to change
      OCP - extend without editing
      LSP / ISP / DIP - depend on interfaces
    Extensibility test
      New type = one new class
      Zero edits to existing classes
      Interfaces for interchangeable behaviour
    Code-review round
      Walk entities then services
      Why this pattern problem it solves
      How would you add feature X
```

## #2 Design Patterns (Strategy / State / Factory / Observer / Decorator)
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Design Patterns Strategy / State / Factory / Observer / Decorator))
    Strategy
      Swap algorithm at runtime
      Pricing / ranking / allocation
      Interface + concrete strategies
    State
      Lifecycle transitions
      Vending machine, order status
      Each state = a class
    Factory / Abstract Factory
      Create by type without new-in-code
      Payment methods, notification channels
      Registry of creators
    Observer / Pub-Sub
      Notify subscribers on change
      Event bus, notifications
      Decouple producer and consumer
    Decorator / Chain
      Layer behaviour dynamically
      Validation chain, middleware
      Composable wrappers
```

## #3 In-memory Store, Cache & KV (with iterators, TTL, snapshots)
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((In-memory Store, Cache and KV with iterators, TTL, snapshots))
    Base builds
      LRU - hashmap + doubly linked list
      LFU - frequency buckets
      KV store with hit counter
    Expiry and eviction
      TTL - lazy vs active sweep
      Weight/size-bounded eviction
      Eviction during iteration
    Versioning
      Snapshot array - store version,value
      Time-based KV - value at timestamp
      Get value as-of time t
    Persistence
      Serialize / deserialize
      Custom encoding length-prefix
      Restore after crash
    Concurrency Concept 6
      Thread-safe get/put
      Striped locks vs global lock
      Iterators over a mutating map
```

## #4 Rate Limiter, Scheduler & Concurrency Control
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Rate Limiter, Scheduler and Concurrency Control))
    Rate-limit algorithms
      Token bucket
      Sliding window log / counter
      Fixed window counter
      Leaky bucket
    Scheduler
      Delayed / periodic tasks
      Priority scheduling
      Job queue with workers
    Concurrency Concept 6
      Atomics / CAS vs locks
      Bounded blocking queue
      Condition variables, no lost wakeups
    Distributed follow-ups
      Per-key limits across nodes
      Clock skew + grace windows
      Redis / shared store fallback
    Correctness
      Idempotency under retries
      Fairness / starvation
      Persist across restarts
```

## #5 Event Systems, Notification & Pub-Sub
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Event Systems, Notification and Pub-Sub))
    Core
      Publisher / Subscriber registry
      Topic / event routing
      Sync vs async dispatch
    Delivery
      Multi-channel email/SMS/push
      Factory per channel
      Template method for send
    Reliability
      Retry with backoff
      Dead-letter queue
      At-least-once vs exactly-once
    Throttling
      Per-user rate limiting
      Batching / coalescing
      Priority / quiet hours
    Correctness
      Unsubscribe / cleanup no leaks
      Ordering guarantees
      Idempotent delivery
```

## #6 Concurrency Primitives in LLD (thread-safety follow-ups)
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Concurrency Primitives in LLD thread-safety follow-ups))
    Primitives
      Mutex / read-write lock
      Atomic / compare-and-swap
      Condition variable
      Semaphore / lock striping
    Patterns
      Producer-consumer bounded buffer
      Thread-safe cache / counter
      Double-checked locking
      Read-copy-update
    Pitfalls
      Deadlock / livelock
      Lost wakeups
      ABA problem
      False sharing / starvation
    Scaling
      Lock-free via CAS
      Sharded locks for throughput
      Backpressure via bounded queues
    Testing
      Deterministic interleavings
      Stress tests
      Invariants under every interleaving
```

## #7 Parsers, Interpreters, Tokenizers & Rule Engines
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Parsers, Interpreters, Tokenizers and Rule Engines))
    Tokenize
      Lexer - keywords / symbols
      Trie or regex scanner
      Longest-match tokens
    Parse
      Recursive descent
      Shunting-yard / precedence
      Build an AST
    Evaluate
      Stack machine
      AST walk / visitor
      Short-circuit operators
    Rule engines
      Composable predicates
      AND/OR/NOT trees
      Data-driven rules
    Robustness
      Precise error positions
      Malformed input handling
      Extensible grammar
```

## #8 Booking, Inventory & Reservation Systems
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Booking, Inventory and Reservation Systems))
    Entities
      Resource / seat / slot
      Reservation lifecycle
      Inventory counts
    Allocation
      Search available
      Hold with expiry
      Confirm / cancel / release
    Consistency
      No double-booking
      Atomic reserve
      Optimistic vs pessimistic locking
    Pricing
      Dynamic / tiered pricing Strategy
      Discounts / coupons
      Surge / demand-based
    Edge cases
      Hold expiry cleanup
      Partial group booking
      Overbooking policy
```

## #9 Games, Simulations & State Machines
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Games, Simulations and State Machines))
    Entities
      Board / grid / cells
      Players and turns
      Pieces / tokens with rules
    Moves
      Move validation
      Legal-move generation
      Undo / redo
    State
      State pattern for lifecycle
      Turn management
      Win / draw / termination
    Rules
      Configurable rules
      Special cases check/mate
      Rule engine separate from board
    Scaling
      k players / n x n board
      Real-time vs turn-based
      Concurrency for multiplayer
```

## #10 File Systems, Iterators & Custom Collections
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((File Systems, Iterators and Custom Collections))
    Structures
      In-memory filesystem tree
      Nested list / document
      Lazy / deferred collection
    Iterators
      Flatten nested iterator
      Resumable get_state/set_state
      2D / 3D / multi-file
    Laziness
      Deferred evaluation
      Memoize once
      Testable laziness
    Operations
      mkdir / addFile / ls / find
      Path resolution
      Glob / search
    Robustness
      Empty files / dirs
      Mutation during iteration
      Corner cases in next /hasNext
```

## #11 AI-coding, Agentic & Take-home Rounds (2026)
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((AI-coding, Agentic and Take-home Rounds 2026))
    Formats
      Take-home project
      Beta agentic round large repo
      Timed IDE build
    AI-tool rules
      Allowed - Cursor / Claude Code xAI
      Banned - most OpenAI + Anthropic live
      Confirm with recruiter first
    What they grade
      Scoping a real feature
      Clean, tested, runnable code
      Communication / write-up
    Practices
      TDD - tests first
      Small commits / clear structure
      README + trade-off notes
    Traps
      Over-engineering
      Ignoring tests
      Not reading the codebase first
```

## #12 Testing, Extensibility & the Code-Review Round
```mermaid
---
config:
  theme: base
  darkMode: true
  themeVariables:
    primaryColor: "#2D3250"
    primaryTextColor: "#E6E6F0"
    primaryBorderColor: "#7A86B6"
    lineColor: "#7A86B6"
    textColor: "#E6E6F0"
    fontSize: "15px"
    cScale0: "#F76C6C"
    cScale1: "#F9A26C"
    cScale2: "#5DA3FA"
    cScale3: "#4ECDC4"
    cScale4: "#A78BFA"
    cScale5: "#F6D365"
    cScaleLabel0: "#1A1A2E"
    cScaleLabel1: "#1A1A2E"
    cScaleLabel2: "#1A1A2E"
    cScaleLabel3: "#1A1A2E"
    cScaleLabel4: "#1A1A2E"
    cScaleLabel5: "#1A1A2E"
---
mindmap
  root((Testing, Extensibility and the Code-Review Round))
    Driver / demo
      main exercises key flows
      Readable, runnable first-try
      Happy path end-to-end first
    Testing
      Unit-test the seams
      Name edge cases explicitly
      TDD where they weight it
    Extensibility
      New type = one new class
      Open-closed via interfaces
      No edits to existing code
    Edge cases
      Empty / full / invalid input
      Concurrency race points
      Error handling / validation
    Code review
      Walk entities then services
      Why this pattern problem solved
      'With more time I'd add...'
```
