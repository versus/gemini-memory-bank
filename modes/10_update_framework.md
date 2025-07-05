# Mode: Update Framework

**Objective**: To autonomously update the framework from a new version, preserving all user data.

## Process

1.  **Identify New Version Source**: The user must provide the absolute path to the directory containing the new framework version.
2.  **Version Check**:
    *   Read `manifest.json` from the source directory and the current directory.
    *   Compare their `version` fields. If the new version is a downgrade, ask the user for explicit confirmation before proceeding. Abort if they decline.
3.  **Confirm Update Scope**:
    *   Clearly state which files will be updated (core logic, prompts) and which will be preserved (`project_board.md`, `session_memory.md`, `session_log.md`, and the `backup/` directory).
4.  **Autonomous Backup**:
    *   Inform the user: "I am creating a secure backup of your data before proceeding."
    *   Execute the following command using your tools:
        *   `run_shell_command("mkdir -p backup && cp project_board.md session_memory.md session_log.md backup/backup-$(date +%F-%T)")`
5.  **Autonomous Update**:
    *   Inform the user: "I am now updating the framework files."
    *   Execute the `rsync` command using your tools. **You must replace `/path/to/update/` with the actual path provided by the user.**
        *   `run_shell_command("rsync -av --exclude='project_board.md' --exclude='session_memory.md' --exclude='session_log.md' --exclude='backup/' /path/to/update/ .")`
    *   This command guarantees that user data is never overwritten.
6.  **Verify and Finalize**:
    *   Confirm that the `manifest.json` in the current directory now matches the version of the source directory.
    *   Inform the user: "The framework has been successfully updated to version [new_version]. Your data was preserved and backed up."
7.  **Re-bootstrap Framework**:
    *   To complete the update, you must now re-initialize the system.
    *   Immediately execute the instructions from `bootstrap.md` to load the new framework version.
