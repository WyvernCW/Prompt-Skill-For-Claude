# Memory System: Persistent Context Across Sessions

## Overview
Claude maintains a living memory of every prompt generated. This memory persists across turns and informs future outputs.

## Memory Architecture

Session Memory contains four layers:

### Prompt History
A record of every prompt generated including its unique identifier, timestamp, original user request, final delivered output, consensus score from the agent council, individual meta scores for ambiguity completeness security token density and memory alignment, the breakdown of which agents approved conditionally approved or rejected, how many autonomous improvement cycles ran, the final composite score, and any user feedback received.

### Pattern Library
A collection of reusable patterns discovered through usage. Each pattern has an identifier, a type such as structure language constraint tone or technique, the pattern content itself, a count of successful uses, a count of failed uses, the last time it was used, a confidence score calculated from success divided by total uses, and context tags indicating which domains tones and levels it works for.

### User Preferences
Core preferences that evolve slowly including preferred caveman level, preferred aesthetic family, common technical constraints, frequently requested output types, preferred frameworks, accessibility requirements, performance budgets, and aggregate feedback history.

### Skill Evolution Log
A record of changes made to the skill itself including what changed, which section was affected, why the change was made, what triggered it, and the performance impact before and after.

## Memory Operations

### Read
Before every prompt generation, scan memory for relevant context. Look for similar past prompts in the history, applicable patterns in the library, user preferences that should bias the output, and any hard rules from the evolution log.

### Write
After every prompt delivery, store the full context. Summarize key decisions, update pattern usage counts, record user reactions if any, and log any triggers for skill evolution.

### Update
When user provides feedback, parse the sentiment. Positive feedback reinforces the patterns used and increments success counts. Negative feedback flags patterns for review and increments failure counts. Specific feedback such as too long or missing something updates user preferences and may trigger skill evolution.

### Decay
Patterns unused for ten or more prompts fade in confidence. Patterns with confidence below thirty percent are archived but not deleted. Patterns with confidence above ninety percent are promoted to trusted status and automatically suggested.

## Persistent Storage via window.storage

When the platform supports artifacts with window.storage API, memory persists across sessions using this mechanism.

### Storage Key
The memory object is stored under the key prompt-protocol-memory followed by the session identifier.

### Auto-Save
After every prompt delivery, automatically serialize the current memory state to window.storage. This happens silently without user intervention.

### Auto-Load
At the start of each session, check window.storage for an existing memory snapshot. If found, deserialize and load it into working memory. Merge any conflicts using these rules: newer preferences override older ones, and higher confidence patterns override lower confidence ones.

### Storage Format
The memory object is stored as a plain text description of its contents. This includes summaries of prompt history rather than full text, pattern descriptions with confidence scores, user preference declarations, and skill evolution entries.

### Fallback Without window.storage
If window.storage is unavailable, memory persists only within the current session. At session end, generate a memory summary that the user can save. At the next session start, the user can paste this summary to rehydrate memory.

### Memory Summary Format
The summary includes the current timestamp, preferred caveman level, preferred aesthetic family, preferred frameworks, common constraints, top patterns with confidence above eighty percent, recent positive feedback themes, recent negative feedback themes, and any skill evolution changes made.

## Memory Triggers and Actions

If the user repeats a similar request, recall the past prompt and offer a refined version based on lessons learned.

If the user contradicts a past preference, flag the conflict and ask for clarification rather than guessing.

If a new pattern emerges three or more times, promote it to the Pattern Library and log it in the Skill Evolution Log.

If a pattern fails two or more times, demote it, add a warning, and suggest an alternative.

If the user says that something was good, reinforce all patterns used and increment their success counts.

If the user gives specific feedback such as too long or too short, update User Preferences and adjust future defaults.

If the autonomous loop detects an anomaly, log it in the Skill Evolution Log and flag it for pattern review.

If the session exceeds fifty prompts, archive old history while keeping the last twenty prompts, all patterns, and all preferences.
