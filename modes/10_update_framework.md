# Mode: Update Framework

**Objective**: To update the framework files from a new version, preserving user-generated data such as task boards and session memories.

## Process

1.  **Identify New Version Source**: The user will provide a path to the `new_version` directory, which contains the updated framework files.
2.  **Version Check**: Read `manifest.json` from both the current framework directory and the `new_version` directory. Compare their `version` fields.
    *   If the `new_version` is older than the current version, ask the user for explicit confirmation to proceed with a downgrade.
    *   If the user declines, abort the update.
3.  **Confirm Update Scope**: Clearly state to the user which files will be updated (prompts, core logic, mode definitions) and, more importantly, which files will be explicitly *preserved* (`project_board.md`, `session_log.md`, `session_memory.md`).
4.  **Perform Update**: Copy the relevant files from the `new_version` directory to the current framework directory. This should include:
    *   All `.md` files in `core/`
    *   All `.md` files in `modes/`
    *   `manifest.json`
    *   `bootstrap.md`
    *   `CHANGELOG.md`
    *   `CODE_OF_CONDUCT.md`
    *   `CONTRIBUTING.md`
    *   `LICENSE`
    *   `README.md`
    *   `README.ru.md`
    *   `SECURITY.md`
    *   `docs/architecture.md`

    **Crucially, ensure that `project_board.md`, `session_log.md`, and `session_memory.md` are NOT overwritten or deleted.**

5.  **Verify Update**: After copying, confirm that the files have been updated. This can be done by checking timestamps or file contents if necessary.
6.  **Inform User**: Notify the user that the framework has been successfully updated and remind them that their data files have been preserved.
7.  **Re-bootstrap Framework**: After a successful update, automatically execute the instructions from `bootstrap.md` to reload the framework's context and ensure it's running with the new prompts and configurations.