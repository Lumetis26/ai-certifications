# Daily Workflows

## Summary

Anthropic recommends following a structured development workflow when using Claude Code: **Explore → Plan → Code → Commit**. This process helps Claude understand your project before making changes, encourages thoughtful planning, uses testing to validate implementation, and finishes with code review and source control. Managing Claude's context effectively and leveraging features like subagents, automated commit workflows, and session recovery further improves productivity and keeps long-running development sessions efficient.

---

## Learning Objectives

By the end of this module, you should be able to:

- Explain the Explore → Plan → Code → Commit workflow.
- Use Plan Mode to safely analyze changes before implementation.
- Define clear success criteria for Claude Code.
- Manage Claude's context window effectively.
- Use context management commands during development.
- Understand when to use subagents.
- Improve code quality through AI-assisted code reviews.
- Streamline Git workflows using Claude Code's built-in features.

---

## Key Concepts

### The Explore → Plan → Code → Commit Workflow

Anthropic recommends approaching software development as four distinct phases:

```text
Explore
    ↓
Plan
    ↓
Code
    ↓
Commit
```

Each phase provides an opportunity to validate assumptions before moving to the next stage, reducing unnecessary rework and improving implementation quality.

---

### Explore

Before writing code, Claude should understand the existing project.

During the Explore phase, Claude can:

- Read project files
- Analyze application architecture
- Locate relevant code
- Trace existing workflows
- Search documentation
- Gather implementation context

The objective is to fully understand the problem before proposing a solution.

---

### Plan

Plan Mode allows Claude to analyze the project using read-only tools before making changes.

A good implementation plan identifies:

- Files that will change
- Required dependencies
- Implementation strategy
- Potential risks
- Areas needing clarification

Since no files are modified during planning, this is the safest stage to revise requirements and adjust the approach.

---

### Code

Once the plan is approved, Claude begins implementation.

During this phase Claude can:

- Modify source code
- Create new files
- Refactor existing functionality
- Execute terminal commands
- Run automated tests
- Troubleshoot problems
- Iterate until the objective is achieved

Development becomes an interactive collaboration between you and Claude rather than a one-time prompt.

---

### Define Success Criteria

Claude performs best when success is clearly defined.

Good success criteria include:

- Expected functionality
- Acceptance criteria
- Design requirements
- Performance expectations
- Test results

Clearly defining "done" allows Claude to verify its own work more effectively.

---

### Use Development Tools

Additional tools expand what Claude can accomplish.

Examples include:

- Browser automation
- UI testing
- Documentation lookup
- Build tools
- External services
- MCP servers

Providing the right tools reduces manual back-and-forth and improves automation.

---

### Test Everything

A reliable automated test suite becomes Claude's source of truth.

Claude can:

- Execute existing tests
- Generate new tests
- Validate implementations
- Detect regressions
- Troubleshoot failures

Reliable testing significantly improves Claude's ability to verify completed work.

---

### Save Project Knowledge

Store recurring project information in **CLAUDE.md**.

Examples include:

- Coding standards
- Architecture notes
- Common commands
- Development workflows
- Troubleshooting steps
- Team conventions

This prevents Claude from rediscovering the same information during future sessions.

---

## Context Management

### The Context Window

The context window is Claude's working memory.

It includes:

- Conversation history
- Source code
- File contents
- Tool results
- Command output
- Previous reasoning

Because context is finite, efficient management becomes important during long development sessions.

---

### Automatic Compaction

When the context window approaches its limit, Claude automatically compacts the conversation by:

- Summarizing important information
- Removing unnecessary details
- Preserving key decisions
- Freeing memory for additional work

Although compaction retains the important information, some fine-grained details may be lost.

---

### Context Commands

Claude Code provides several commands for managing context.

#### `/compact`

Summarizes the current conversation while preserving important information.

Use when:

- Working on a long feature
- Approaching the context limit
- Continuing the same implementation

---

#### `/clear`

Starts a completely new session.

Use when:

- Beginning a new feature
- Switching projects
- Eliminating previous conversational bias

---

#### `/context`

Displays information about the current context window, including:

- Overall usage
- Categories consuming context
- Visual usage breakdown

This helps determine when context management is necessary.

---

### Saving Context

To maximize available context:

- Write specific prompts.
- Disable unused MCP servers.
- Use Skills when appropriate.
- Delegate isolated tasks to subagents.
- Store permanent project knowledge in `CLAUDE.md`.

Being more specific actually saves context because Claude spends less time exploring your project to determine your intent.

---

## Subagents

Subagents operate independently from the primary Claude session.

Each subagent has:

- Its own context window
- Independent reasoning
- Separate tool usage

The main Claude session receives only the summarized results, keeping the primary context focused and efficient.

Subagents are ideal for:

- Code reviews
- Codebase exploration
- Finding files
- Research
- Documentation lookup

---

## Code Review

Before committing code, Anthropic recommends using a dedicated code-reviewer subagent.

Unlike the primary agent, the reviewer:

- Starts with a fresh context
- Has no implementation bias
- Reviews changes objectively
- Identifies potential issues

For safety, reviewer subagents should use **read-only tools** so they can identify problems without modifying code.

---

## Git Workflow Automation

### `/commit-push-pr`

Claude Code includes a built-in workflow that automates:

1. Commit
2. Push
3. Pull Request creation

If configured, Claude can also notify your team through integrations such as Slack.

---

### Resume Work with `--from-pr`

Claude sessions can be linked directly to pull requests.

To continue working later:

```bash
claude --from-pr <PR_NUMBER>
```

This restores the previous working context, making it easy to address review comments or continue unfinished work.

---

## Best Practices

- Always explore the project before requesting implementation.
- Use Plan Mode for complex or multi-step features.
- Define clear success criteria before coding begins.
- Give Claude access to reliable development tools.
- Maintain an automated test suite.
- Store project-specific knowledge in `CLAUDE.md`.
- Monitor your context usage during long sessions.
- Use `/compact` to continue long features.
- Use `/clear` before starting unrelated work.
- Use subagents for specialized tasks.
- Run an unbiased code review before committing.
- Automate commits and pull requests where appropriate.

---

## Key Takeaways

- Anthropic's recommended workflow is **Explore → Plan → Code → Commit**.
- Planning before implementation significantly reduces unnecessary rework.
- Claude verifies its work more effectively when success criteria and tests are clearly defined.
- The context window is a limited working memory that should be actively managed.
- `/compact`, `/clear`, and `/context` help manage long-running development sessions.
- Subagents improve efficiency by performing isolated tasks with their own independent context.
- A dedicated code-reviewer subagent provides an unbiased review before code is committed.
- Built-in Git features such as `/commit-push-pr` and `--from-pr` streamline daily development workflows.

---

## Lumetis Applications

Potential applications include:

- AI-assisted feature planning
- Large-scale code refactoring
- Technical architecture reviews
- Automated testing workflows
- Internal code review automation
- Git workflow standardization
- Development documentation
- Knowledge management through `CLAUDE.md`
- Software quality assurance
- AI-assisted engineering workflows

---

## Personal Notes

### Mental Model

Treat Claude Code like an experienced software engineer following a disciplined development process rather than a code generator.

Successful development follows this pattern:

**Explore → Plan → Code → Verify → Review → Commit**

The goal is not simply to generate code, but to understand the problem, implement the right solution, verify the results, review the work objectively, and commit with confidence. Managing context, defining success clearly, and leveraging subagents allows Claude Code to remain effective even on large, long-running software projects.
