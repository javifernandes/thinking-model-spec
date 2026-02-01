# Higher-Order Functions (HOF)

> **Node status:** Draft v1 — grounded in Part III ("Naming and Abstraction") of the book.

## Why this node exists

Higher-order functions are the moment where *naming* stops being just labeling and becomes **structural abstraction**. They allow behavior itself to be named, passed, delayed, combined, and manufactured. This is the inflection point where programs stop being sequences of steps and become systems of interchangeable parts.

In the book, HOFs emerge naturally from a prior insight: once naming gives us power over transformations, the next step is to treat those transformations as *things*.

## Prerequisites (soft, experiential)

These do not need to be formally mastered, but must be *felt*:

* Functions as named transformations (apply_move as paradigm)
* Purity and referential transparency (trust in names)
* Delegation: callers rely on contracts, not implementations

## Core definition (book-aligned)

A higher-order function is a function that:

* **takes one or more functions as input**, and/or
* **returns a function as output**.

In the book’s framing: **verbs become nouns**. Actions become manipulable values.

## How the book introduces the idea (conceptual path)

1. **Naming as power**: Naming a transformation creates an abstraction boundary.
2. **Trust via purity**: Pure functions make names reliable promises.
3. **Functions as values**: A function can be referred to *without being called*.
4. **Delegation of behavior**: Systems accept functions that decide *how* to act.
5. **Factories and memory**: Functions can produce other functions that remember.

HOFs are not introduced as a formal leap, but as the *inevitable consequence* of earlier ideas.

## Recognition signals ("you are doing HOFs when...")

* You choose behavior at runtime by selecting a function.
* A function’s parameters include *decisions*, not just data.
* Control flow moves outward; inner logic becomes replaceable.
* You say: "the game loop doesn’t know *which* strategy it’s using."
* You build pipelines where functions chain other functions.

## Canonical patterns from the book

### 1. Strategy as value

```text
opponent_strategy = random_move | greedy_move | defensive_move
move = opponent_strategy(state)
```

Behavior is selected, stored, and invoked later.

### 2. Behavior parameterization

```text
play_game(initial_state, white_player, black_player)
```

The system is configured by *supplying functions*.

### 3. Function factories

```text
make_multiplier(2) → double
make_multiplier(3) → triple
```

Functions are produced dynamically.

### 4. Closures (functions that remember)

* Returned functions carry private state.
* Each invocation creates an isolated world.

## Common misconceptions (explicit)

* "HOFs are just map/filter/reduce" → Those are *instances*, not the idea.
* "They are only for functional languages" → The book shows them in neutral pseudo-code.
* "They are about cleverness" → They are about *delegation and modularity*.
* "Closures are magic" → They are memory + function, nothing more.

## Exercise archetypes (derived from prose)

### A. Parameterize the decision

* Replace conditionals with function arguments.
* Same system, different behavior.

### B. Extract the transformation

* Take a concrete loop and lift the varying part into a function.

### C. Build a strategy space

* Multiple small functions, selected dynamically.

### D. Manufacture behavior

* Write a function that returns a customized function.

### E. Recognition exercise

* Reader unknowingly uses an HOF; system later names it.

## Difficulty progression

1. Passing a named function
2. Passing an anonymous function
3. Returning a function
4. Closures with memory
5. Composing HOFs

## Visualization hooks

* Function boxes containing smaller function boxes
* Flow diagrams where *functions* appear as data nodes
* Parallel runs showing same structure, different behavior

## Book grounding (traceability)

Primary source: Part III — "Naming and Abstraction"

* "The Power of Names"
* "Verbs Become Nouns"
* Delegation via chess strategies
* Closures via make_multiplier / make_counter

## System hooks (for later layers)

* **Exercise generator**: must respect seen prerequisites
* **Reader model**: detect unintentional HOF usage
* **AI tutor**: trigger "what you just did is called..." moments
* **Graph links**: connects to Naming, Delegation, Closures, Polymorphism
