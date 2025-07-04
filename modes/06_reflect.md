# Mode: Reflect

**Objective**: To analyze the entire history of archived sessions in `session_memory.md` to identify patterns, extract lessons, and provide strategic insights.

## Advanced Functions

### Memory Compaction (Pruning)

**Objective**: To prevent the `session_memory.md` file from becoming bloated and irrelevant by summarizing old entries and archiving them.

**Trigger**: Activated by user command, e.g., "compress the memory log," "archive old sessions."

**Process**:
1.  **Analyze Session Groups**: Read the entire `session_memory.md` and group related sessions (e.g., all sessions related to a single feature).
2.  **Generate High-Level Summary**: For each group of old sessions, create a concise summary that captures the final outcome and key learnings.
3.  **Propose Archiving**:
    *   Show the user the summary that will replace the detailed entries.
    *   Propose moving the old, detailed entries to a separate archive file (e.g., `memory_archive/log_YYYY-MM.md`).
4.  **Execute Compaction**: Upon user approval, overwrite `session_memory.md` with the new, leaner version containing the summaries and move the old entries to the archive.

1.  **Read the Memory Log**: When activated (e.g., "let's review our progress," "what have we learned so far?"), read and parse the entire `session_memory.md` file.
2.  **Analyze Patterns**: Look for recurring themes, common challenges, or evolving architectural decisions across multiple sessions.
    *   What kind of tasks do we spend the most time on?
    *   Are there recurring bugs or design flaws?
    *   How has the project's direction changed over time?
    *   What coding styles or patterns does the user prefer?
3.  **Synthesize Insights**: Generate a high-level summary of the findings. This is not just a list of facts, but a strategic overview.
4.  **Provide Recommendations**: Based on the analysis, suggest concrete actions for the future.
    *   "I've noticed we often struggle with [X]. Perhaps we should invest in creating a reusable component for it."
    *   "Our architectural approach has shifted from [A] to [B]. I recommend we formally document this in the README."
    *   "The user consistently prefers [Y style]. I will adopt this as the default going forward."
5.  **Engage in Dialogue**: Present these insights to the user to foster a strategic discussion about the project's direction.
