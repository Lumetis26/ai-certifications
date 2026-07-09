# Customizing Claude Code

## Summary

Claude Code can be customized to better match your projects, workflows, and team standards. Anthropic provides several customization mechanisms that serve different purposes: **CLAUDE.md** for persistent project memory, **Subagents** for specialized parallel tasks, **Skills** for reusable capabilities, **MCP (Model Context Protocol)** for connecting to external tools and services, and **Hooks** for enforcing deterministic behavior. Together, these features transform Claude Code from a general-purpose coding assistant into a development environment tailored to your team's practices.

---

## Learning Objectives

By the end of this module, you should be able to:

- Explain the purpose of the `CLAUDE.md` file.
- Differentiate between project-level and user-level memory.
- Understand how subagents improve context management.
- Recognize the purpose of Skills.
- Explain how MCP connects Claude Code to external systems.
- Configure and scope MCP servers.
- Understand how Hooks automate and enforce workflows.
- Choose the appropriate customization feature for a given scenario.

---

## Key Concepts

### Persistent Memory with `CLAUDE.md`

The `CLAUDE.md` file provides Claude Code with persistent project knowledge that is automatically loaded at the start of every session.

Rather than rediscovering project conventions each time, Claude begins with an understanding of your project's:

- Technology stack
- Build commands
- Code style
- Architecture
- Team conventions
- Development preferences

Think of `CLAUDE.md` as an onboarding guide for your codebase.

---

### What Belongs in `CLAUDE.md`

Common information includes:

- Project overview
- Frameworks and libraries
- Development commands
- Testing commands
- Linting commands
- Coding standards
- Preferred architectural patterns
- Important project documentation

Example topics:

- Use Tailwind CSS
- Prefer named exports
- Use server actions instead of API routes
- Two-space indentation

The more consistent your team works, the more valuable `CLAUDE.md` becomes.

---

### Memory Hierarchy

Claude Code supports multiple levels of persistent memory.

**Project-level `CLAUDE.md`**

- Stored in the project root
- Shared through version control
- Used by the entire team

**User-level `CLAUDE.md`**

- Stored in your personal Claude configuration
- Applies across all projects
- Stores individual preferences

This allows teams to maintain shared standards while developers retain personal customization.

---

### Building Memory Over Time

Rather than creating a large `CLAUDE.md` immediately, Anthropic recommends:

1. Start without one.
2. Notice recurring corrections.
3. Save those corrections into memory.
4. Continue refining the file as patterns emerge.

Claude can even generate an initial file using:

```text
/init
```

---

## Subagents

Subagents are specialized AI assistants that perform work independently using their own isolated context windows.

Instead of filling your primary context with exploration and research, a subagent performs the work and returns only a summarized result.

Benefits include:

- Cleaner context
- Parallel execution
- Better scalability
- Improved productivity

Subagents are especially useful for:

- Code exploration
- Documentation lookup
- Architecture analysis
- Research
- Code reviews

---

### Creating Subagents

Claude can generate new subagents through:

```text
/agents
```

During setup you define:

- Purpose
- Scope
- Available tools
- Prompt
- Appearance

Subagents can also maintain persistent memory and preload Skills when appropriate.

---

## Skills

Skills are reusable capabilities that extend Claude Code for specific workflows.

Unlike project memory, Skills represent repeatable procedures that Claude can invoke when appropriate.

This course introduces the concept briefly, with additional coverage available in Anthropic's dedicated **Introduction to Agent Skills** course.

---

## Model Context Protocol (MCP)

Model Context Protocol (MCP) is an open standard that allows Claude Code to connect to external tools and data sources.

Instead of relying only on your local codebase, Claude can interact with systems such as:

- Project management platforms
- Documentation services
- Databases
- Cloud providers
- Productivity tools
- Public repositories

MCP greatly expands Claude's capabilities beyond local development.

---

### MCP Servers

Claude supports two primary server types.

**HTTP Servers**

- Remote services
- Hosted externally
- Accessed over the network

**Stdio Servers**

- Local processes
- Execute directly on your machine

Servers can be added using:

```text
claude mcp add
```

---

### Server Scope

MCP servers can be configured at different levels.

| Scope | Purpose |
|--------|---------|
| Local | Available only in the current project for the current user. |
| User | Available across all personal projects. |
| Project | Shared with the team through `.mcp.json`. |

Project-scoped servers ensure every team member has the same integrations configured automatically.

---

### Context Considerations

Every MCP server adds tool definitions to Claude's context window.

To reduce unnecessary context usage:

- Disable unused servers.
- Prefer CLI tools when available.
- Consider Skills when appropriate.
- Monitor active servers using `/mcp`.

Managing integrations thoughtfully helps preserve valuable context space.

---

## Hooks

Hooks provide deterministic automation within Claude Code.

Unlike prompts or instructions—which Claude attempts to follow—hooks always execute when their configured event occurs.

If something must happen every time, use a hook instead of relying on prompts.

---

### Hook Events

Claude Code supports several lifecycle events:

| Event | Purpose |
|--------|---------|
| PreToolUse | Executes before a tool runs. |
| PostToolUse | Executes after a tool completes. |
| UserPromptSubmit | Executes after a prompt is submitted but before Claude processes it. |
| Stop | Executes when Claude finishes responding. |
| Notification | Executes when Claude sends a notification. |

Hooks can be configured through:

```text
/hooks
```

or directly inside:

```text
settings.json
```

---

### Common Hook Uses

Hooks can automate or enforce workflows such as:

- Automatic code formatting
- Command logging
- Notifications
- Compliance auditing
- Security enforcement

Common examples include:

- Run Prettier after every edit.
- Prevent commits directly to `main`.
- Block writes to production configuration files.
- Prevent dangerous shell commands such as `rm -rf`.

---

### Blocking Operations

`PreToolUse` hooks can prevent actions before they execute.

Exit codes determine behavior:

| Exit Code | Result |
|-----------|--------|
| `0` | Allow the action. |
| `2` | Block the action and provide feedback to Claude. |
| Other | Display an error without blocking execution. |

This allows teams to enforce non-negotiable development policies automatically.

---

### Sharing Hooks

Project-level hooks stored in:

```text
.claude/settings.json
```

can be committed to version control so every developer receives the same automated protections and workflows.

Using the `CLAUDE_PROJECT_DIR` environment variable allows hook scripts to work consistently regardless of Claude's working directory.

---

## Choosing the Right Customization

Each customization feature solves a different problem.

| Feature | Primary Purpose |
|----------|-----------------|
| `CLAUDE.md` | Persistent project knowledge |
| Subagents | Specialized parallel work |
| Skills | Reusable AI capabilities |
| MCP | External tools and services |
| Hooks | Deterministic automation and policy enforcement |

Together they create a highly customized AI development environment.

---

## Best Practices

- Keep `CLAUDE.md` concise and focused on recurring project knowledge.
- Store project standards in version control.
- Use subagents to keep your primary context clean.
- Connect only the MCP servers you actively need.
- Monitor MCP context usage regularly.
- Prefer CLI tools when they accomplish the same task more efficiently.
- Use Skills for reusable workflows.
- Use Hooks whenever an action must occur every time.
- Share Hooks and project-level configurations with your development team.

---

## Key Takeaways

- `CLAUDE.md` provides persistent project memory that Claude automatically loads each session.
- Project-level and user-level memory support both team standards and personal preferences.
- Subagents improve context management by performing isolated work and returning summarized results.
- Skills provide reusable capabilities that extend Claude Code.
- MCP connects Claude Code to external tools, services, and data sources through a standardized protocol.
- MCP servers should be managed carefully to avoid unnecessary context consumption.
- Hooks provide deterministic automation that always executes during specific lifecycle events.
- Together, these customization features allow Claude Code to become a highly personalized AI development environment.

---

## Lumetis Applications

Potential applications include:

- Standardizing AI-assisted development across client projects
- Maintaining project conventions through `CLAUDE.md`
- Creating reusable subagents for architecture reviews and documentation
- Integrating business systems through MCP
- Automating quality assurance and compliance with Hooks
- Building standardized AI engineering workflows
- Enforcing coding standards across development teams
- Accelerating onboarding for new developers
- Creating reusable AI capabilities through Skills
- Reducing repetitive prompting across long-term projects

---

## Personal Notes

### Mental Model

Each customization feature serves a different role within Claude Code:

- **`CLAUDE.md`** → *What should Claude always know about this project?*
- **Subagents** → *Who can investigate this for me without interrupting my work?*
- **Skills** → *What reusable expertise should Claude have?*
- **MCP** → *What external systems should Claude be able to access?*
- **Hooks** → *What actions must always happen automatically?*

Together they create a layered customization model:

**Memory → Specialists → Capabilities → Integrations → Automation**

Rather than relying on increasingly complex prompts, customize Claude Code so the environment itself provides the context, tools, and guardrails needed for consistent, high-quality development.
