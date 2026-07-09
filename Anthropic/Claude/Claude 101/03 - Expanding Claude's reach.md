# Claude 101

## Module 3: Expanding Claude's Reach

## Summary

Module 3 focuses on extending Claude beyond a standalone AI assistant by connecting it to the tools, documents, and systems you already use. Through **Connectors**, **Enterprise Search**, and **Research**, Claude gains access to relevant context, organizational knowledge, and external information, allowing it to deliver more accurate, actionable, and comprehensive results.

The key idea throughout this module is simple:

> **The more relevant context Claude has, the more valuable it becomes.**

Rather than copying and pasting information between applications, Claude can securely access connected services, combine information from multiple sources, and perform complex research with citations.

---

# Lesson 1: Connectors

## Summary

Connectors allow Claude to securely interact with cloud services and desktop applications, transforming it from a conversational assistant into an AI collaborator that works directly with your existing tools.

Instead of manually providing context every time, Claude can retrieve information, analyze documents, create content, and perform actions within supported applications.

Connectors are powered by the **Model Context Protocol (MCP)**, an open standard that functions much like USB-C for AI—providing a consistent interface between Claude and external applications.

---

## Learning Objectives

By the end of this lesson you should be able to:

- Explain what Connectors are
- Understand how MCP powers integrations
- Connect cloud services and desktop applications
- Use connected tools within conversations
- Understand connector permissions and security

---

## Key Concepts

### Connectors Extend Claude's Context

Without connectors:

- Claude only knows what you provide during the conversation.

With connectors:

- Claude can securely access the same information you already work with.

Examples include:

- Gmail
- Google Drive
- Slack
- Notion
- Asana
- Jira
- Stripe
- Salesforce
- PayPal
- Microsoft 365
- SharePoint

---

### Two Types of Connectors

#### Web Connectors

Cloud-based services.

Examples:

- Gmail
- Slack
- Google Drive
- Notion
- Asana
- Stripe

Setup involves:

1. Selecting the connector
2. Logging into the service
3. Granting permissions
4. Using it immediately inside Claude

---

#### Desktop Extensions

Require Claude Desktop.

These provide access to:

- Local files
- Native applications
- Browser automation
- Desktop integrations

Examples include:

- Local document management
- Browser control
- Design tools such as Figma

---

### MCP (Model Context Protocol)

MCP is an open protocol that standardizes communication between Claude and external applications.

Benefits include:

- One universal integration standard
- Easier connector development
- Consistent user experience
- Expanding ecosystem of supported tools

---

## Practical Use Cases

### Project Management

Claude can:

- Summarize project status
- Review upcoming tasks
- Create new work items
- Identify blockers

---

### Communication

Claude can:

- Search email threads
- Summarize Slack discussions
- Draft replies
- Find previous conversations

---

### Documentation

Claude can:

- Search documentation
- Summarize meeting notes
- Find policies
- Locate style guides

---

### Business Systems

Claude can:

- Review revenue trends
- Check CRM opportunities
- Analyze transactions
- Summarize financial information

---

## Security

Important principles:

- Permissions are scoped.
- Claude only accesses information you already have permission to view.
- Access can be revoked at any time.
- Only install trusted connectors.

---

## Key Takeaways

- Connectors eliminate repetitive copy-and-paste workflows.
- Claude becomes significantly more useful when it understands your existing work.
- MCP provides a scalable, standardized integration framework.
- Security remains permission-based and user-controlled.

---

# Lesson 2: Enterprise Search

## Summary

Enterprise Search is designed specifically for organizations using Claude Team or Enterprise plans.

Instead of searching individual tools manually, Enterprise Search searches across your company's connected knowledge sources and produces a single synthesized answer with citations.

Think of it as asking your entire organization a question instead of searching dozens of applications yourself.

---

## Learning Objectives

By the end of this lesson you should be able to:

- Explain Enterprise Search
- Understand organizational setup
- Use Enterprise Search effectively
- Understand security and permissions

---

## Key Concepts

### Organization-Wide Knowledge

Enterprise Search combines information from:

- Slack
- Google Drive
- SharePoint
- Gmail
- Microsoft 365
- Internal documentation
- Other enterprise connectors

---

### Best Use Cases

Enterprise Search excels at:

- Company policies
- Internal processes
- Project history
- Meeting summaries
- Organizational knowledge
- Onboarding
- Cross-team research

---

### Example Questions

- What changed while I was out yesterday?
- What are the blockers for Project X?
- What is our remote work policy?
- Summarize discussions about our roadmap.
- How does our deployment process work?

---

## Setup

### Admin Responsibilities

Admins:

- Enable Enterprise Search
- Connect company systems
- Configure the project
- Select data sources

---

### User Responsibilities

Users:

- Authenticate personal accounts
- Connect approved services
- Begin asking questions

---

## Security

Enterprise Search follows existing organizational permissions.

Claude:

- Cannot access data users cannot access
- Doesn't expose restricted information
- Doesn't create a separate searchable copy of company data
- Keeps conversations private

---

## Key Takeaways

- Enterprise Search centralizes organizational knowledge.
- It reduces time spent searching multiple systems.
- Responses include citations.
- Existing permissions remain fully enforced.

---

# Lesson 3: Research

## Summary

Research transforms Claude into an autonomous research assistant capable of conducting multi-step investigations across the web and connected integrations.

Rather than performing a single search, Claude plans an investigation, performs multiple searches, synthesizes findings, and delivers a structured report with citations.

Complex research that might normally require several hours can often be completed within minutes.

---

## Learning Objectives

By the end of this lesson you should be able to:

- Understand how Research works
- Know when to use Research
- Write better Research prompts
- Combine Research with connected integrations

---

## Key Concepts

### Agentic Research

Research works differently from normal chat.

Claude:

- Plans the investigation
- Performs multiple searches
- Identifies new questions
- Follows promising leads
- Synthesizes information
- Produces a comprehensive report

---

### Extended Thinking

Research automatically enables Extended Thinking.

Claude first reasons about:

- What information is needed
- Where to find it
- Which questions require additional investigation

before beginning the research process.

---

### Multi-Step Workflow

Research follows four stages:

1. Plan
2. Search
3. Synthesize
4. Cite Sources

---

## When to Use Research

Ideal for:

- Market research
- Competitive analysis
- Vendor comparisons
- Technical documentation
- Executive briefings
- Industry analysis
- Complex planning

---

## When NOT to Use Research

Use:

### Web Search

For:

- Quick facts
- Simple lookups
- Current information

---

### Extended Thinking

For:

- Logic
- Mathematics
- Programming
- Problem solving

without needing outside information.

---

### Enterprise Search

For:

- Company knowledge
- Internal documentation
- Slack discussions
- Policies
- Organizational context

---

## Effective Research Prompts

Strong prompts should include:

### Clear Goals

Define exactly what you're trying to learn.

---

### Desired Structure

Specify sections you'd like included.

Example:

- Executive Summary
- Findings
- Recommendations
- Risks
- Sources

---

### Constraints

Include:

- Budget
- Timeline
- Geography
- Industry
- Audience

---

### Refinement

Claude can even help improve your research prompt before beginning the investigation.

---

## Connected Integrations

Research becomes even more powerful when combined with connected services.

Examples:

- Analyze internal emails alongside industry research.
- Compare company strategy against competitors.
- Review calendar meetings while researching attendees.
- Combine Google Drive documents with current web research.

---

## Key Takeaways

- Research performs autonomous multi-step investigations.
- Extended Thinking is automatically enabled.
- Reports include verifiable citations.
- Connected integrations provide richer context.
- Research dramatically reduces manual investigation time.

---

# Overall Module Takeaways

Module 3 demonstrates how Claude evolves from an AI assistant into a connected intelligence platform.

The three major capabilities build on one another:

| Feature | Primary Purpose |
|----------|-----------------|
| **Connectors** | Give Claude access to your tools and applications. |
| **Enterprise Search** | Search and synthesize knowledge across your organization. |
| **Research** | Perform deep, multi-source investigations with citations. |

Together, these capabilities allow Claude to:

- Work with real organizational data
- Eliminate repetitive context sharing
- Search across multiple systems simultaneously
- Conduct autonomous research
- Produce comprehensive reports with citations
- Save hours of manual investigation while maintaining security and permission boundaries

---

## Core Principle

> **Claude becomes exponentially more useful as it gains secure access to the information and systems you already use. The combination of Connectors, Enterprise Search, and Research enables Claude to move beyond answering questions toward becoming a true AI collaborator that works within your existing workflows.**
