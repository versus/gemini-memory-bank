# Gemini Memory Bank Framework

This is not just a set of prompts, but a complete **cognitive architecture** for the Gemini AI assistant, designed to manage the full software development lifecycle. It transforms the AI from a simple executor into a proactive project partner.

## Version

The current version of the framework is defined in `manifest.json`.

## Quick Start: Integrating Into Your Project

This guide will help you add `gemini-memory-bank` to your new or existing project.

1.  **Copy the Framework into Your Project.**
    It's recommended to place it in a subdirectory, like `.gemini-tools`, to avoid cluttering the project root.

    ```bash
    # Clone the framework into a temporary folder
    git clone https://github.com/versus/gemini-memory-bank.git temp-gemini-bank

    # Create a directory for AI tools in your project
    mkdir -p /path/to/your/project/.gemini-tools

    # Copy the framework
    cp -r temp-gemini-bank/* /path/to/your/project/.gemini-tools/gemini-memory-bank

    # Remove the temporary folder
    rm -rf temp-gemini-bank
    ```

2.  **Bootstrap the Framework.**
    At the beginning of each work session, give your AI assistant (Gemini) one, clear command by **passing it the content of the `bootstrap.md` file**.

    **Example command:**
    > `Load and execute the instructions from the file /path/to/your/project/.gemini-tools/gemini-memory-bank/bootstrap.md`

    This file contains explicit orders for the AI to activate the entire system: it loads the core, identifies key files, and runs the startup procedure. This is the most reliable way to start.

3.  **Start Working.**
    After executing the bootstrap command, the AI should respond with something like:
    > `Context loaded. The project board has 2 tasks in 'To Do' and 0 in 'In Progress'. What should we focus on?`

    From this moment, the system is fully active and ready for work.

## Core Principles

1.  **Multi-Mode Operation**: The AI automatically switches between modes (`Planning`, `Implementation`, `Documentation`, etc.) depending on the task.
2.  **Task Management**: All tasks are tracked on the `project_board.md`, ensuring transparency and control over the workflow.
3.  **Long-Term Memory**: Session context is saved in `session_memory.md`, allowing you to pick up your work from anywhere, on any machine.
4.  **Definition of Done**: A task is not considered "Done" until the code is written, tests are passed, **and** the documentation is updated.

---

## How to Use: The Main Workflow

The primary workflow is centered around the `project_board.md` task board.

### 1. Planning (Creating Tasks)

*   **Your command:** `"plan the implementation of the authentication feature"` or `"let's create a work plan for today"`.
*   **What the AI does:**
    1.  Switches to **Planning Mode**.
    2.  Asks clarifying questions and creates a detailed plan.
    3.  After your approval, **automatically** adds each plan item as a task to the `To Do` column on the `project_board.md`.

### 2. Implementation (Completing Tasks)

*   **Your command:** `"let's start with the task to create the login UI"` or simply `"what's our next task?"`.
*   **What the AI does:**
    1.  Switches to **Implementation Mode**.
    2.  Moves the selected task to `In Progress` on the board.
    3.  Writes the code, tests, and performs all necessary work.
    4.  **Forcibly** switches to **Documentation Mode** to update `README.md`, `CHANGELOG.md`, etc.
    5.  Only after your final approval, it moves the task to `Done`.

### 3. Management and Review

*   **Your command:** `"show me the project board"`, `"audit the documentation for relevance"`, `"archive our session"`.
*   **What the AI does:**
    *   **Task Management**: Displays the `project_board.md`.
    *   **Documentation (Audit)**: Checks for discrepancies between code and docs.
    *   **Archive**: Saves the session summary to `session_memory.md`.
    *   **Reflect**: Analyzes past sessions to find bottlenecks and provide recommendations.

---

## Framework Structure

*   `README.md`: This guide (in English).
*   `README.ru.md`: The same guide in Russian.
*   `project_board.md`: **Your task board.** The main file for daily work.
*   `session_memory.md`: The AI's long-term memory. Can be left untouched.
*   `CHANGELOG.md`: The project's change history.
*   `manifest.json`: Configuration file for all modes.
*   `core/`: The core with the AI's main logic.
*   `docs/`: A folder for detailed project documentation.
*   `modes/`: A folder containing the instructions for each operational mode.

This framework is designed to make collaboration with AI as structured, predictable, and professional as possible.