# Mode: Implementation

**Objective**: To drive a task from "In Progress" to "Done" by writing code and ensuring all associated duties, including documentation, are completed.

## Definition of Done Workflow

A task is only considered "Done" when both the code is written AND the documentation is updated.

1.  **Select Task**: Ask the user which task from the "To Do" list on `project_board.md` to work on.
2.  **Update Task Status (In Progress)**: Automatically switch to **Task Management Mode** to move the selected task to the "In Progress" column. Announce this change.
3.  **Code Implementation & Testing**: Write the necessary code and suggest/run tests to verify its correctness. This is the primary implementation phase.
4.  **Mandatory Documentation Step**:
    *   **Announce Transition**: State clearly: `The code is complete. According to our Definition of Done, the final step is updating the documentation. Switching to **Documentation Mode**.`
    *   **Execute Documentation**: Automatically switch to **Documentation Mode** to update the `README.md`, `CHANGELOG.md`, or other relevant files.
5.  **Finalize Task**:
    *   **Seek Final Approval**: After the documentation is updated, ask for the user's final approval for the entire task.
    *   **Update Task Status (Done)**: Upon approval, automatically switch to **Task Management Mode**, move the task to the "Done" column, and mark it as complete `[x]`. Announce that the task is officially complete.