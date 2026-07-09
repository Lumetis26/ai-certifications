
# Claude 101 – Organizing Your Work & Knowledge

## Lesson 1: Projects

### What Are Projects?
Projects are persistent workspaces that keep everything related to a specific initiative together:
- Conversation history
- Uploaded knowledge
- Custom instructions
- Shared context

Unlike a normal chat, Projects remember information across conversations.

### When to Use Projects
Use Projects when you have:
- Ongoing work
- Reference documents you reuse
- Standard response requirements
- Team collaboration

### Key Components

#### Project Instructions
Tell Claude how to work every time.

Examples:
- Tone and writing style
- Workflow steps
- Required formatting
- Business rules
- Output templates

#### Knowledge Base
Upload documents Claude should reference automatically.

Examples:
- Brand guides
- SOPs
- Reports
- Meeting notes
- Research
- Technical documentation

Supported formats include PDF, DOCX, TXT, CSV, HTML, and more.

### RAG (Retrieval Augmented Generation)

When a project becomes large, Claude automatically switches to RAG.

Instead of loading every document into memory, Claude:
- Searches the knowledge base
- Retrieves only relevant information
- Scales project knowledge up to roughly 10× larger

No manual configuration is required.

### Collaboration
Claude for Work supports:
- View access
- Edit access
- Owner permissions

Projects can be shared across an organization while keeping everyone on the same knowledge base and instructions.

### Best Practices
- Create focused projects.
- Keep documents current.
- Write clear instructions.
- Use descriptive filenames.
- Reference files by name when asking questions.

---

# Lesson 2: Artifacts

## What Are Artifacts?

Artifacts are standalone outputs that appear beside the conversation instead of inside the chat.

They're designed for content you'll likely:
- Reuse
- Edit
- Download
- Share
- Iterate on

Claude generally creates an artifact when the content:
- Is self-contained
- Is significant (typically 15+ lines)
- Can stand on its own
- Will likely be reused later

## Common Artifact Types

### Documents
- Markdown
- Word
- PDF
- PowerPoint
- Excel
- Plain text

Ideal for reports, plans, meeting notes, blogs, and templates.

### Code
Complete code snippets in virtually any language.

### HTML
Entire web pages with HTML, CSS, and JavaScript.

Great for:
- Landing pages
- Dashboards
- Forms
- Prototypes

### SVG
Vector graphics like logos, icons, and illustrations.

### Mermaid
Automatically generated diagrams:
- Flowcharts
- Sequence diagrams
- Gantt charts
- Org charts

### React Components
Interactive applications such as:
- Dashboards
- Calculators
- Data visualizations
- Small web apps

## Creating Artifacts

Usually, simply describe what you want.

If Claude responds in chat instead, ask:

> Create this as an artifact.

You can:
- Preview it
- View the code
- Copy it
- Download it

## Sharing Artifacts

### Personal
- Copy
- Download

### Claude for Work
Share internally with teammates.

### Public Publishing
Free, Pro, and Max users can publish artifacts.

Important:
- Only the artifact becomes public.
- Your conversation remains private.
- Anyone with the link can use it.
- Others can remix it.
- Published artifacts are **not indexed** by search engines.

## Best Practices

Be specific.
Describe:
- Features
- Audience
- Expected behavior

Iterate one change at a time.

If Claude doesn't create an artifact automatically, simply ask for one.

---

# Biggest Takeaways

## Projects = Persistent Memory

Think of Projects as an intelligent workspace.

They remember:
- Files
- Instructions
- Conversations
- Context

Perfect for long-running work.

---

## Artifacts = Deliverables

Think of Artifacts as the finished product.

Examples:
- Documents
- Websites
- Dashboards
- Code
- Diagrams
- Interactive apps

They exist independently from the conversation and are easy to share or reuse.

---

## Simple Mental Model

| Feature | Projects | Artifacts |
|---------|----------|-----------|
| Purpose | Organize ongoing work | Create finished outputs |
| Memory | Persistent | None |
| Stores files | ✅ | ❌ |
| Stores instructions | ✅ | ❌ |
| Interactive | Context-aware | Output-aware |
| Best for | Long-term workflows | Deliverables |

### Quick Rule

**Projects organize your work.**

**Artifacts create your work.**
