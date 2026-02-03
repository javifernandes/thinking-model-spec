# Architecture Overview

This document explains the conceptual architecture of the project.

It is **not an implementation guide**.
It describes:
- the levels of abstraction
- how probes work
- how systems are explored and evolved
- how tooling gradually emerges

The goal is to make the project understandable, extensible, and evolvable.


# Levels of Abstraction

```mermaid
flowchart TB
    VISION["VISION<br/>Meta-models, methodology,<br/>how systems are explored"]
    SYSTEM["SYSTEM<br/>A concrete system definition<br/>(e.g. Learning System)"]
    DOMAIN["DOMAIN / BOOK<br/>A specific instantiation<br/>(Programming, Martial Arts, etc.)"]
    RUNTIME["RUNTIME EXPERIENCE<br/>Live learner sessions,<br/>signals, feedback"]

    VISION --> SYSTEM
    SYSTEM --> DOMAIN
    DOMAIN --> RUNTIME
```

Explanation

* Vision defines how systems are described, explored, and evolved.
* System defines what exists in a given system (entities, axes, workflows).
* Domain / Book instantiates the system with real content.
* Runtime Experience is the live execution with real users.


# What a Probe Is

A probe is an executable experiment over a system.
It is not content, not tooling, and not a test.

```mermaid
flowchart LR
    PROBE["Probe<br/>(Declaration)"]
    SYSTEM["System Definition"]
    CAPS["Capabilities<br/>(Pluggable)"]
    OUTPUT["Probe Artifacts<br/>(Evidence, Signals,<br/>Insights, Gaps)"]

    PROBE --> SYSTEM
    PROBE --> CAPS
    CAPS --> OUTPUT
```

## Key idea

A probe:
* declares what is being explored
* declares which capabilities are required
* produces structured artifacts

It can run **without a real product**.

# Capabilities: Progressive Concretization

Capabilities are **replaceable execution surfaces**.
They are defined by contract, not implementation.

```mermaid
flowchart TB
    PROBE["Probe"]
    CAPSET["Capability Set"]

    CAP1["Content Presenter"]
    CAP2["Learner Input Capture"]
    CAP3["Interpretation Engine"]
    CAP4["Evaluation Engine"]
    CAP5["Feedback Emitter"]

    PROBE --> CAPSET
    CAPSET --> CAP1
    CAPSET --> CAP2
    CAPSET --> CAP3
    CAPSET --> CAP4
    CAPSET --> CAP5
```

Each capability may have multiple implementations:

```mermaid
flowchart LR
    CAP["Content Presenter"]

    LLM["LLM Simulation"]
    CLI["CLI Renderer"]
    HTML["Static HTML"]
    UI["UI Prototype"]

    CAP --> LLM
    CAP --> CLI
    CAP --> HTML
    CAP --> UI
```

The probe **does not** care which one is used.

# Wizard-of-Oz → System Evolution

The same probe can run at increasing levels of realism.

```mermaid
timeline
    title Progressive Realism of Probes
    Phase 1 : Pure LLM simulation
    Phase 2 : Human + LLM hybrid
    Phase 3 : Mock UI artifacts
    Phase 4 : Partial real system
    Phase 5 : Fully implemented system
```

This allows:
* early discovery
* cheap failure
* gradual commitment


# Example: Author → Learner → System Flow

```mermaid
sequenceDiagram
    participant Author
    participant Interpreter
    participant System
    participant Learner

    Author->>Interpreter: Write source content
    Interpreter->>System: Generate draft concepts, axes, motifs
    System->>Learner: Present content & exercises
    Learner->>System: Interact, answer, explore
    System->>System: Emit signals & feedback
    System->>Author: Surface insights & gaps
```

This closes the loop **without requiring a finished platform**.


# Capability Gaps & Insights

Probes produce **structured findings**, not opinions.

```mermaid
flowchart LR
    SIGNALS["Signals"]
    INSIGHTS["Insights"]
    GAPS["Capability Gaps"]
    SPECS["Spec Evolution"]

    SIGNALS --> INSIGHTS
    INSIGHTS --> GAPS
    GAPS --> SPECS
```

A capability gap means:

> “To run this probe faithfully, the system needs a capability it doesn’t yet have.”

This guides __what to build next__, without premature implementation.

