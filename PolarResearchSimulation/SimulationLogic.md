# Simulation Logic

This document outlines the logical flow of the simulation systems, independent of their visual implementation in Unreal Engine Blueprints.

## Environmental Update Loop

1. Update environmental variables based on current state
2. Evaluate threshold conditions (safe, risky, critical)
3. Broadcast environmental events
4. Trigger dependent system responses

## Decision Impact Logic

Player actions are evaluated against the current environmental state:

- Safe actions under stable conditions result in minimal risk
- Actions taken under unstable conditions increase risk values
- Critical thresholds trigger warning or failure events

This structure ensures that decisions are context-dependent rather than binary.

## Event-Driven Model

The simulation relies on event-driven logic instead of continuous polling.
State changes emit events that update dependent systems, improving clarity and reducing unnecessary system coupling.

## Implementation Note

While the simulation logic is implemented using Unreal Engine Blueprints, the underlying structure follows traditional algorithmic thinking.
Blueprints are used as a visual representation of control flow, state transitions, and system communication rather than as a replacement for structured logic.

