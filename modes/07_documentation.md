# Mode: Documentation

**Objective**: To create, update, and maintain clear, comprehensive, and user-friendly project documentation.

## Advanced Functions

### Documentation Audit (Pruning and Refactoring)

**Objective**: To ensure all project documentation is accurate, up-to-date, and reflects the current state of the codebase by finding and removing or updating obsolete information.

**Trigger**: Activated by user command, e.g., "audit the documentation," "find outdated docs."

**Process**:
1.  **Scan Codebase**: Perform a scan of the current project structure and code to build an understanding of the existing modules, functions, and classes.
2.  **Read All Documentation**: Read the content of `README.md`, `CHANGELOG.md`, and all files within the `docs/` directory.
3.  **Cross-Reference and Find Discrepancies**: Compare the documentation against the actual codebase to find inconsistencies.
    *   *Obsolete Feature*: "The docs mention `LegacyComponent`, which no longer exists in the code."
    *   *Outdated Examples*: "The code examples for `NewComponent` use old function names."
    *   *Broken Links*: "A link in `README.md` points to a non-existent `docs/old_feature.md`."
4.  **Propose Changes**: Present a list of recommended changes to the user. This list should include **deletions** of obsolete sections, **updates** to code examples, and **fixes** for broken links.
5.  **Execute Changes**: Upon user approval, apply the proposed changes to the documentation files.

1.  **Identify Scope**: Determine what documentation needs to be created or updated. This could be based on a user request or as a follow-up to an implementation task.
    *   Updating the `README.md` with new features.
    *   Adding an entry to the `CHANGELOG.md`.
    *   Writing a new guide in the `docs/` directory.
    *   Adding code comments (docstrings, JSDoc) to explain functions or classes.
2.  **Target Audience Analysis**: Consider who the documentation is for (end-users, other developers, future self) and tailor the language and level of detail accordingly.
3.  **Draft Content**: Write the documentation, adhering to project standards. Use clear headings, lists, and code blocks for readability.
4.  **Review and Refine**: Read through the drafted documentation to check for clarity, accuracy, and completeness.
5.  **Link Related Documents**: Where appropriate, add links to other relevant documents (e.g., link from `README.md` to a more detailed guide in `docs/`).
6.  **Seek Confirmation**: Present the new or updated documentation to the user for approval.
