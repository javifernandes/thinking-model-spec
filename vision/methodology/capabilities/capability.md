# Capabilities

A capability defines a **minimal interaction or operation** that must exist
for a probe to be executed.

Capabilities are:
- declarative
- implementation-agnostic
- reusable across probes

A probe does not implement capabilities.
It **requires** them.

Examples:
- present_content_to_learner
- capture_free_text_input
- interpret_with_llm
- emit_feedback_event

Capabilities may later be:
- simulated manually
- executed via Wizard-of-Oz
- implemented in software

Only capabilities that recur across probes
should be promoted into the system layer.
