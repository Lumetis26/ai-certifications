## Your First Prompt

Claude Code uses prompts the same way other AI assistants do, but the difference is that your prompt can lead to real actions inside your codebase. Because Claude Code can edit files and run commands, it is important to choose the right permission mode and give clear instructions before work begins.

---

## Learning Objectives

By the end of this lesson, you should be able to:

- Understand the difference between Approval Mode and Auto-Accept Mode.
- Use Plan Mode before making complex changes.
- Write a clear first prompt for Claude Code.
- Review Claude's plan before allowing it to make changes.
- Stay in control while Claude works through implementation tasks.

---

## Key Concepts

### Prompting Claude Code

You can talk to Claude Code like any other AI assistant, but prompts should be more descriptive because Claude can take action directly inside your project.

A strong Claude Code prompt should include:

- What you want changed
- Where the change should appear
- Any design or technical constraints
- Whether Claude should plan first
- How you want the result verified

---

### Approval Mode

In Approval Mode, Claude asks for permission before editing files or running commands.

This mode is useful when:

- You are new to Claude Code.
- You want to review every change.
- You are working in an unfamiliar codebase.
- The task could affect important files.

Approval Mode keeps you closely involved throughout the process.

---

### Auto-Accept Mode

In Auto-Accept Mode, Claude automatically approves file edits, but terminal commands still require permission.

This mode is useful when:

- You trust the scope of the task.
- The project is low-risk.
- You want fewer interruptions.
- You are comfortable reviewing changes afterward.

There is no universally correct mode. The right choice depends on the task, the project, and your comfort level.

---

### Switching Modes

You can switch between permission modes by pressing:

```text
Shift + Tab
```

This allows you to cycle between available modes, including Approval Mode, Auto-Accept Mode, and Plan Mode.

---

### Plan Mode

Plan Mode uses read-only tools to inspect the project and create a detailed plan before making any changes.

In Plan Mode, Claude can:

- Analyze the codebase
- Research the implementation
- Ask clarifying questions
- Identify affected files
- Propose a step-by-step approach

Plan Mode is especially useful for complex changes, multi-step features, and safe code reviews.

---

### Example: Dark Mode Toggle

A good first prompt might be:

```text
My app needs a dark mode implemented across the entire app. Can you create a toggle switch on the header that allows a user to toggle between light mode and dark mode? I need you to find a good contrast color that works based on my existing light theme.
```

This prompt works because it includes:

- The feature being requested
- Where the UI change should appear
- The expected behavior
- A design constraint
- Permission for Claude to inspect the existing theme

Claude can then analyze the project, create a plan, and request approval before making changes.

---

## Best Practices

- Be descriptive with your prompt.
- Use Plan Mode for larger or riskier changes.
- Review Claude's plan before approving implementation.
- Use Approval Mode when you want to stay involved at every step.
- Use Auto-Accept only when the task is low-risk or you are comfortable reviewing changes afterward.
- Let Claude explain what it changed and why after the work is complete.

---

## Key Takeaways

- Claude Code prompts can lead to real project changes, not just text responses.
- Approval Mode keeps you involved before every file edit or command.
- Auto-Accept Mode reduces interruptions by automatically approving file edits.
- Terminal commands still require permission even in Auto-Accept Mode.
- Plan Mode is useful for analyzing complex changes before execution.
- Clear, descriptive prompts produce better plans and safer implementation.
