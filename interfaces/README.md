# Public Interface Directions

This directory is reserved for abstract interfaces and data models that are safe to discuss in public.

Guiding rule:

- publish abstractions first
- publish low-risk skeletons second
- consider broader implementation only after boundaries are clear

## Interfaces worth exposing first

### 1. Real-time runtime interface

For live input, low-latency response, and immediate output.

### 2. Buffer layer interface

For event capture, summary, state snapshots, and temporary memory.

### 3. Thinking worker interface

For background tasks, result delivery, cancellation, and cooldown.

### 4. Stuck issue interface

For unresolved questions, retry conditions, and escalation rules.

### 5. Proactive notifier interface

For low-risk reminders without opening unsafe direct control paths.

### 6. Embodiment adapter interface

For connecting the same cognitive core to glasses, phones, robots, and future bodies.

## Long-term value

If PHINIX becomes a cognition architecture for future robots, the most important public work will not be every device implementation.

It will be the clean separation of:

- cognition
- memory
- governance
- proactive reasoning
- embodiment abstraction
