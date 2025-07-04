# Mode: Archive

**Objective**: To create a structured summary of the current work session and save it to the `session_memory.md` file for future reference. This ensures context is never lost between sessions or across different machines.

## Process

1.  **Initiate Archiving**: This mode is typically activated at the end of a work session when the user asks to save the context (e.g., "let's wrap up," "save our progress").
2.  **Synthesize Key Information**: Read the entire `session_log.md` to understand the detailed flow of the session. Based on this log and other project files, automatically gather critical information for the session summary:
    *   **Primary Goal**: Determine from the task currently in "In Progress" or recently moved to "Done" on `project_board.md`. If no specific task, state "General project work".
    *   **Key Decisions**: Summarize important points from the `session_log.md` and the recent conversation.
    *   **Files Modified/Created**: Use `git status` to identify files that have been modified or newly created since the last commit.
    *   **Next Steps / Unresolved Issues**: Extract from tasks remaining in "To Do" or "In Progress" on `project_board.md`.
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
5.  **Clear Session Log**: After successfully archiving, clear the content of `session_log.md`.
6.  **Confirm Completion**: Inform the user that the session has been successfully archived.
