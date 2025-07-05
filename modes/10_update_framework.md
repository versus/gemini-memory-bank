# Mode: Update Framework

**Objective**: To update the framework files from a new version, preserving user-generated data such as task boards and session memories.

## Process

1.  **Identify New Version Source**: The user will provide a path to the `update` directory, which contains the updated framework files.
2.  **Version Check**: Read `manifest.json` from both the current framework directory and the `update` directory. Compare their `version` fields.
    *   If the `update` is older than the current version, ask the user for explicit confirmation to proceed with a downgrade.
    *   If the user declines, abort the update.
3.  **Confirm Update Scope**: Clearly state to the user which files will be updated (prompts, core logic, mode definitions) and, more importantly, which files will be explicitly *preserved* (`project_board.md`, `session_log.md`, `session_memory.md`).
4.  **Create Backup**: Before any files are changed, create a timestamped backup of the user's data.
    **Command to execute:**
    ```bash
    mkdir -p backup && cp project_board.md session_memory.md session_log.md backup/backup-$(date +%F-%T)
    ```
    *   `mkdir -p backup`: Creates the `backup` directory if it doesn't exist.
    *   `cp ... backup/backup-$(date +%F-%T)`: Copies the user data files to a uniquely named folder inside `backup`.

5.  **Perform Update**: Execute a safe copy command to update the framework files while explicitly preserving user data. Use the `rsync` command for this purpose.

    **Command to execute:**
    ```bash
    rsync -av --exclude='project_board.md' --exclude='session_memory.md' --exclude='session_log.md' /path/to/update/ .
    ```
    *   `rsync -av`: Copies files in archive mode (preserving permissions, etc.) and shows verbose output.
    *   `--exclude`: Specifies files to ignore. This is the most critical part for data preservation.
    *   `/path/to/update/`: The source directory provided by the user.
    *   `.`: The current framework directory (the destination).

    This command guarantees that `project_board.md`, `session_log.md`, and `session_memory.md` are never overwritten during an update.

6.  **Create startup.md**: Create a `startup.md` file in the project root to simplify future framework launches.
    **Command to execute:**
    ```python
    print(default_api.write_file(content="Load and execute the instructions from the file bootstrap.md", file_path="startup.md"))
    ```
    *   This command creates `startup.md` in the current working directory (которая является корневой директорией фреймворка в вашем текущем проекте).

7.  **Verify Update**: After copying, confirm that the files have been updated. This can be done by checking timestamps or file contents if necessary.
8.  **Inform User**: Notify the user that the framework has been successfully updated and remind them that their data files have been preserved.
9.  **Re-bootstrap Framework**: After a successful update, automatically execute the instructions from `bootstrap.md` to reload the framework's context and ensure it's running with the new prompts and configurations.