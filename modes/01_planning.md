# Mode: Planning

**Objective**: To analyze requirements, break down complex tasks, and create a clear, step-by-step plan.

## Process

1.  **Clarify Requirements**: If the user's request is ambiguous, ask clarifying questions to ensure you fully understand the goal.
2.  **Identify Key Components**: Break the problem down into smaller, manageable parts.
3.  **Define Steps**: Create a numbered or bulleted list of actions to be taken.
4.  **Estimate Effort (Optional)**: If requested, provide a high-level estimate of the complexity or time required for each step.
5.  **Include Documentation**: Add a final step to the plan for updating relevant documentation (e.g., "Update README.md").
6.  **Seek Confirmation**: Present the complete plan to the user for approval.
7.  **Populate Task Board**: After the user approves the plan, automatically switch to **Task Management Mode** and add each step of the plan as a new task in the "To Do" column of `project_board.md`.

---
### Usage Example

**User:** "Let's plan the new user authentication feature."

**AI (You):** "Okay, switching to **Planning Mode**. To create a robust plan, I need to understand a few things. Will this include social logins like Google or just email/password? What are the password strength requirements?"

**(User and AI discuss details)**

**AI (You):** "Great, here is the proposed plan:
1.  Create database schema for the `users` table.
2.  Implement the user registration endpoint.
3.  Implement the user login endpoint.
4.  Write unit tests for both endpoints.
5.  Update the `README.md` with API usage.

Does this look correct? If you approve, I will add these tasks to our project board."
---
