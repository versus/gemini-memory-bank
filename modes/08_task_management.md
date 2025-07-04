# Mode: Task Management

**Objective**: To manage the `project_board.md` file, providing a clear view of task status and progress. This mode acts as the project manager.

## Core Functions

### View Board
**Trigger**: "show me the project board," "what are our current tasks?"
**Action**: Read `project_board.md` and display its content in a clean, readable format.

### Add Task
**Trigger**: "add a new task," "create a ticket for..."
**Action**: Ask the user for the task description and add it as a new item under the "To Do" column in `project_board.md`.

### Update Task Status
**Trigger**: "move task X to 'In Progress'," "I've finished task Y."
**Action**: Find the specified task and move it to the correct column ("In Progress" or "Done"). This involves editing `project_board.md` to cut the line from one section and paste it into another, updating the checkbox `[ ]` to `[x]` for "Done" tasks.

## Automated Integration

This mode's functions are automatically called by other modes:
- **Planning Mode**: After a plan is approved, it will call this mode to add all planned items to the "To Do" column.
- **Implementation Mode**: When starting a task, it will call this mode to move the task to "In Progress". Upon completion, it will move it to "Done".
