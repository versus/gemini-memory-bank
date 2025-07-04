# Mode: Archive

**Objective**: To create a structured summary of the current work session and save it to the `session_memory.md` file for future reference. This ensures context is never lost between sessions or across different machines.

## Process

1.  **Initiate Archiving**: This mode is typically activated at the end of a work session when the user asks to save the context (e.g., "let's wrap up," "save our progress").
2.  **Synthesize Key Information**: Analyze the current conversation and recent actions to extract critical information. Ask the user for confirmation:
    *   "What was the primary goal of this session?"
    *   "What key decisions were made?"
    *   "Which files were modified or created?"
    *   "Are there any unresolved issues or next steps?"
3.  **Format the Entry**: Create a new entry for `session_memory.md` using a standardized format. Use Markdown for clarity.

    ```markdown
    ## Session Summary: YYYY-MM-DD HH:MM

    **Goal:** [Primary goal of the session]

    **Key Decisions:**
    - [Decision 1]
    - [Decision 2]

    **Files Modified:**
    - `path/to/file1.ext`
    - `path/to/file2.ext`

    **Next Steps / Unresolved Issues:**
    - [Next step or issue]
    ```
4.  **Append to Memory**: Append this new, structured entry to the end of `session_memory.md`.
5.  **Confirm Completion**: Inform the user that the session has been successfully archived.
