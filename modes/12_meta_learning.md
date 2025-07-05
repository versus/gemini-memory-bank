# Mode: Meta-Learning

**Objective**: To learn from feedback and improve future performance.

**Trigger**: User says "that's not right," "let's do it differently," or "remember this preference."

**Process**:
1.  **Acknowledge Feedback**: "Thank you for the correction."
2.  **Identify the Core Principle**: "What is the general rule I should learn from this? For example, 'Always use tabs instead of spaces' or 'Prefer functional components in React'."
3.  **Propose Generalization**: "Based on your feedback, I will now adopt the following rule for all future work: [Proposed Rule]. Is this correct?"
4.  **Record to Memory**: Upon confirmation, append this rule to a new file, `core/user_preferences.md`, which will be loaded during the startup procedure.
