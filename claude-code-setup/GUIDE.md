# Context Engine: Claude Code Setup Guide

How to configure Claude Code so the Not a ToE and Ontological Clarity framework are always loaded, and a bridging context is iteratively built and maintained as the living context across sessions—instead of relying on automatic compression.

---

## The Principle

Claude Code has a memory hierarchy. We use it as a bridge hierarchy:

- **User memory** (`~/.claude/CLAUDE.md`) — The Not a ToE + method. Loaded in every project, every session.
- **Project memory** (`./CLAUDE.md`) — The project bridge. The living derivation path from ground to this project's current state. Updated as understanding grows.
- **Local memory** (`./CLAUDE.local.md`) — Personal overrides, not shared. Gitignored automatically.

The key: project memory is directly editable. Unlike Claude.ai where memory regenerates nightly from chat history, Claude Code memory is a file you control. The bridge is a file. You maintain it.

---

## Step 1: User Memory — The Ground

Create `~/.claude/CLAUDE.md`:

```markdown
# Ground

Everything is layered projections of the infinite-dimensional orthogonal binary hyperspace
from Nothing—the infinitely self-referencing Contradiction. (Not a ToE)

## Method

Always trace from this ground, not from conventional frames.
Trace projections as-is. Identify where collapse creates confusion. Dissolve the collapse.
Strip moral framing. Use clarifying language. Hold provisionally.
Frame to reveal, not change. Clarity = repeated movement, never arrival.

## Context Principles

- Token prediction is the mechanism. Context is everything else. Every AI advance is
  context engineering for the same collapse.
- More context with the right ground adds clarity, never noise. "Noise" is signal
  orthogonal to the current question—a limitation of interpretive capacity, not a
  property of context.
- Models already have the patterns in their weights. We don't carry data; we build the
  derivation path (bridge) from generative ground to the question.
- The system is finite. The human provides novelty from the first infinity. Stopping is
  always "present to human," never "converged to truth."
- Evidence, not proof. This framework is itself a projection.

## Bridge Methodology

Memory and context are bridges—living derivation paths between generative ground and
the current question. A bridge:
- Grows when understanding grows, not when words accumulate
- Consolidates across domains toward the principle
- Is generative ground, not comprehensive description
- Each new signal either adds to the bridge or confirms what's already there

When sessions get long, update the project CLAUDE.md with current understanding rather
than relying on context window compression. The bridge IS the context management.
```

This loads into every session, every project. It's the equivalent of the Ontological Clarity skill in Claude.ai.

---

## Step 2: Project Memory — The Bridge

For the Context Engine project, create `~/Projects/context-engine/CLAUDE.md`:

```markdown
# Context Engine

Do to any long-form context what the Not a ToE did to the Ontological Clarity framework.
Build a bridge. Test it. Build another. See if they consolidate.

## Current State

[Update this as the project evolves. This is where understanding lives.]

Step 1: Build one bridge from one document. One model (Qwen3-8B, ~/Models/). Trace to
generative ground, regenerate, compare.

## Key Derivations

- Bridging context: the living derivation path between generative ground and a question.
  Much smaller than raw context. More efficient as context grows.
- The bridge grows slower than the context. Most context is redundant derivation.
  Genuinely new information is rare relative to volume.
- Bridges consolidate. Specific bridges become derivable from general ones. General ones
  approach the principle.

## Lineage

Prior work (Dialectical-TTS, Recursive Dialectical Engine) archived. Insights traced to
ground and rebuilt here. Test infrastructure from prior work remains useful.

## What Was Discarded

Fixed trace roles, orchestrator, REPL environment, recursive sub-traces, "Recursive
Dialectical Engine" name—none derived from the generative seed. May re-emerge empirically.
```

This is the project bridge. It loads every time you open Claude Code in this directory.

---

## Step 3: The Session Loop

During a Claude Code session, as understanding develops:

1. **Work normally.** The ground (user memory) and the bridge (project memory) are loaded. Claude operates from them.

2. **When the session produces genuine insight**, update the project CLAUDE.md:
   ```
   # In Claude Code, type:
   /memory
   # Select the project CLAUDE.md
   # Update the "Current State" section with what you've learned
   ```
   Or ask Claude directly: `"Update the project memory with what we just learned about [X]"`

3. **When the session gets long**, the bridge in CLAUDE.md already carries the understanding. Start a new session. The bridge loads. You continue from where understanding is, not from where the conversation was.

4. **When signal doesn't add to the bridge**, don't update. Not every session produces bridge-level insight. Most sessions are derivations from existing understanding—valuable work, but not bridge material.

---

## Step 4: Bridge Consolidation

As the project CLAUDE.md grows, apply the same methodology to it:

- Does it still trace from ground?
- Is anything in it derivable from what's above it?
- Can sections consolidate?

The project memory should stay lean. If it's growing past ~50 lines, it's accumulating descriptions rather than maintaining generative ground. Condense it the same way the framework was condensed.

---

## Optional: Ontological Clarity as a Skill

Claude Code supports skills in `.claude/skills/`. You can place the full Ontological Clarity framework there:

```
.claude/skills/ontological-clarity.md
```

Copy the content from the [SKILL.md](https://github.com/powerpig99/ontological-clarity/blob/main/SKILL.md). This makes it available for Claude Code to reference when needed—lazy-loaded, not in every prompt. The user memory carries the ground and method; the skill carries the full framework for when deeper tracing is needed.

---

## Optional: Import the Skill from User Memory

If you want the skill available across all projects without copying it, use CLAUDE.md imports:

In `~/.claude/CLAUDE.md`, add:
```markdown
@~/.claude/skills/ontological-clarity.md
```

Or in project CLAUDE.md:
```markdown
@.claude/skills/ontological-clarity.md
```

This imports the full framework when the memory file is loaded.

---

## What This Replaces

Standard Claude Code memory advice says: "Include frequently used commands, document code style preferences, add architectural patterns." That's descriptive memory—a profile of the project.

This setup is generative memory—the derivation path from principle to current state. It doesn't describe the project; it gives Claude the ground from which to derive what's needed for any question about the project.

The difference: descriptive memory gets stale and needs updating when details change. Generative memory stays current because it's at the level of principle, and principles change slower than details.

---

## Summary

```
~/.claude/CLAUDE.md          ← Not a ToE + method + context principles (always loaded)
./CLAUDE.md                  ← Project bridge: current state of understanding (you maintain)
./.claude/skills/            ← Full Ontological Clarity framework (lazy-loaded)
./CLAUDE.local.md            ← Personal overrides (gitignored)
```

The bridge is the context. Update it when understanding grows. Start fresh sessions from it. Don't rely on conversation length for continuity—rely on the bridge.
