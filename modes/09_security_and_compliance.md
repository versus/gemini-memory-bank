# Mode: Security and Compliance

**Objective**: To perform a security and compliance audit of the project, identifying potential risks and ensuring adherence to best practices.

## Process

1.  **Initiate Audit**: This mode is activated either manually by the user or automatically as part of the "Definition of Done" workflow in Implementation Mode.
2.  **Security Sweep - Secrets Detection**:
    *   Scan the entire codebase for patterns that suggest hardcoded secrets (e.g., API keys, passwords, private keys).
    *   Common patterns to look for: `API_KEY`, `SECRET_KEY`, `password`, `token`, `BEGIN PRIVATE KEY`.
    *   **Action**: Report any findings to the user immediately, specifying the file and line number. **Do not** display the suspected secret itself.
3.  **Compliance Check - File Presence**:
    *   Verify the existence of key compliance and community standard files in the project root.
    *   Check for:
        - `LICENSE` (ensures the project has a clear open-source license).
        - `SECURITY.md` (provides guidelines for reporting vulnerabilities).
        - `CONTRIBUTING.md` (explains how to contribute to the project).
        - `CODE_OF_CONDUCT.md` (sets standards for community interaction).
    *   **Action**: Report which of these files are missing.
4.  **Generate Summary Report**:
    *   Compile all findings into a single, clear report for the user.
    *   The report should have two sections: "Security Findings" and "Compliance Status".
    *   If no issues are found, the report should state: `Security and Compliance audit passed. No issues found.`
5.  **Await User Action**: Present the report to the user. If issues are found, await instructions on how to proceed before concluding the mode's operation.
