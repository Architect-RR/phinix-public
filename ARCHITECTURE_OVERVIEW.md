# Architecture Overview

This document describes the public high-level architecture only. It does not include private deployment details or sensitive bridge configuration.

## Core idea

PHINIX is not just a chatbot and not just a tool-calling agent.

It is closer to:

- a local-first runtime
- an embodied companion core
- a future cognition layer for humanoid systems

## Suggested three-layer architecture

### 1. Real-time layer

Responsibilities:

- receive live input
- produce low-latency responses
- drive immediate interaction

Typical channels:

- voice
- text
- HUD or AR output

### 2. Buffer layer

Responsibilities:

- retain events and conversational context
- build state snapshots
- manage pending issues

Its job is not intelligence first. Its job is:

- capture
- structure
- preserve

### 3. Thinking layer

Responsibilities:

- background reasoning
- stuck-issue revisit
- long-horizon topic tracking
- candidate proactive outputs

This layer should not replace the real-time layer. It should run beside it.

## Stuck issue queue

One of PHINIX's most important ideas is to treat "being stuck" as persistent state rather than a disposable failure.

That allows the system to:

- remember where it failed
- remember what it tried
- revisit the problem later
- surface useful follow-ups when new evidence appears

## Proactive companion behavior

Proactivity should not mean constant interruption.

A healthier flow is:

1. background conclusion appears
2. low-friction reminder is prepared
3. the user chooses whether to expand it

That is closer to a companion than a noise source.

## Why this matters for future robots

If PHINIX is connected to future humanoid systems, its likely role is:

- memory
- issue tracking
- proactive reasoning
- governance
- long-term consistency

Not:

- low-level control
- hard real-time motor control
- a thin SDK wrapper

In that sense, PHINIX is better viewed as a portable cognitive core that can outlive any one device body.
