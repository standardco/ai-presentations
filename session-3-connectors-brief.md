# Session 3 Slide Brief — Claude Connectors (MCP)

## Instructions for Claude in PowerPoint

Create a presentation for Session 3 of the Standard Co 6 Month AI Series. This is a 45-minute, demo-first, practical session. The audience is a mix of developers and non-developers at Standard Co who are already familiar with Claude Code (Session 1) and CLAUDE.md / project context (Session 2). This is their third month — they're bought in but still learning.

Use a clean, modern, professional slide design. Minimal text on slides — the speaker notes carry the detail. Use visuals, diagrams, and short bullet points on the slides themselves.

---

## Terminology — IMPORTANT

- Use **"Connectors"** as the primary term throughout the deck.
- Mention "MCP" (Model Context Protocol) exactly once, early on, as the underlying open protocol. Something like: "Connectors are built on the Model Context Protocol (MCP) — an open standard."
- After that, just say "Connectors" everywhere. The audience doesn't need to think about protocol internals.
- This aligns with Anthropic's own product terminology: in Claude.ai and Claude Desktop, the feature is called "Connectors."

---

## Slide-by-slide outline

### Slide 1: Title slide
- **Title:** Claude Connectors
- **Subtitle:** Connecting Claude to Your Tools
- **Footer:** Standard Co — 6 Month AI Series | Session 3 | May 28, 2026

### Slide 2: Series recap
- **Title:** Where we've been
- **Content:** Simple visual showing the 3-session arc:
  - Session 1 (March): Claude Code + Cowork — met Claude, learned the interface
  - Session 2 (April): CLAUDE.md + ./claude/ — gave Claude project context
  - **Session 3 (May): Connectors — let Claude reach your tools** (highlighted)
- **Speaker notes:** Quick recap. In March we introduced Claude Code and Cowork. In April we talked about how to give Claude lasting project context with CLAUDE.md and the ./claude/ folder. Today we're taking the next step: instead of Claude only working with what's in front of it, we're going to connect it to the tools you already use — Notion, Slack, Google Drive, your internal systems. That's what Connectors are for.

### Slide 3: The problem
- **Title:** Claude is powerful, but isolated
- **Content:** Visual showing Claude in a box, separated from: Notion, Slack, Google Drive, Jira, internal tools, databases
- **Speaker notes:** Out of the box, Claude can only see what you paste into it or what's in your local files. But your real work lives in Notion, Slack, Google Drive, Jira, email, internal dashboards. Every time you copy-paste context into Claude, you're doing the integration work manually. Connectors fix this.

### Slide 4: What are Connectors?
- **Title:** Connectors let Claude use your tools directly
- **Content:** Simple diagram: Claude <---> Connector <---> External Tool (Notion, Slack, etc.)
- **Bullet points:**
  - Claude can read from and write to external tools
  - Built on MCP (Model Context Protocol) — an open standard
  - 200+ pre-built connectors in the Connectors Directory
  - You can also build custom connectors for internal tools
- **Speaker notes:** A Connector is a bridge between Claude and an external service. When you enable a connector, Claude gains the ability to read from and act inside that tool — pull Notion pages, search Slack messages, create Jira tickets, whatever the connector supports. They're built on the Model Context Protocol, or MCP, which is an open standard — but you don't need to know or care about the protocol. Just think of them as plug-and-play integrations. Anthropic maintains a directory of over 200 pre-built connectors, and you can build your own for internal tools.

### Slide 5: Where Connectors work
- **Title:** Available everywhere Claude runs
- **Content:** Grid/icons showing:
  - Claude.ai (web) — Connectors Directory built in
  - Claude Desktop — Connectors + Extensions (local MCP servers)
  - Claude Code (CLI/IDE) — configure in settings or per-project
  - Claude API — MCP Connector parameter for agents
- **Speaker notes:** Connectors aren't limited to one surface. They're available on Claude.ai in the browser, in Claude Desktop, in Claude Code in your terminal or IDE, and even programmatically through the API. The setup differs slightly in each — on Claude.ai you just toggle them on from a directory, in Claude Code you configure them in settings — but the concept is the same everywhere.

### Slide 6: Real use cases at Standard Co
- **Title:** What can you actually do with this?
- **Content:** 4 use case cards:
  1. **Docs & knowledge:** "Pull our Notion wiki pages into Claude to answer questions or draft documents with full context"
  2. **Tickets & project management:** "Have Claude read Jira/Linear tickets, update status, add comments — without leaving your conversation"
  3. **Chat & communication:** "Search Slack history, draft messages, summarize threads"
  4. **Internal tools:** "Connect Claude to internal APIs, dashboards, databases via custom connectors"
- **Speaker notes:** Let's make this concrete. Here are four categories where connectors shine for us. First, docs and knowledge — connect Claude to Notion and it can pull in wiki pages, project docs, meeting notes, and use them as context. No more copy-pasting. Second, tickets — Claude can read your Jira or Linear board, understand what's in progress, update ticket status, even create new tickets from a conversation. Third, chat — connect Slack and Claude can search message history, summarize long threads, or draft replies. Fourth, and this is where it gets really powerful for engineering — you can build custom connectors for your own internal tools. Internal dashboards, databases, deployment systems — anything with an API can become a connector.

### Slide 7: Demo introduction
- **Title:** Let's see it in action
- **Content:** Two demos listed:
  1. Notion Connector — Claude reads and updates Notion tasks, live
  2. End-to-end workflow — connecting to an external source and completing a task
- **Speaker notes:** Enough slides. Let's see this work for real. I'm going to show you two demos. First, we'll use the Notion connector with Claude Code — I'll have Claude pull task information directly from our Notion workspace and update task cards to reflect status. Second, we'll connect Claude to an external source and walk through a complete task end to end.

### Slide 8: DEMO 1 — Notion Connector
- **Title:** Demo: Notion Connector with Claude Code
- **Content:** Screenshot placeholder or minimal text: "Live demo"
- **Speaker notes:** [LIVE DEMO] Open Claude Code. Show the Notion connector configured in settings. Ask Claude to pull the task list from our project board in Notion. Then ask it to update a task's status. Show that the change appears in Notion. Key points to highlight: Claude reads the Notion page structure, understands the task schema, and writes back — all without you leaving the terminal. This is the workflow from Session 2 (CLAUDE.md giving context) combined with Session 3 (connectors giving Claude access to external tools).

### Slide 9: DEMO 2 — End-to-end task with a Connector
- **Title:** Demo: End-to-end with Connectors
- **Content:** Screenshot placeholder or minimal text: "Live demo"
- **Speaker notes:** [LIVE DEMO] Show connecting Claude to a second external source (e.g., Google Drive, Slack, or a relevant internal tool). Walk through a realistic task: maybe pull a document from Google Drive, summarize it, create a Notion task based on it, and post a summary to Slack. The point is to show connectors chained together in a natural workflow — Claude as the hub between your tools.

### Slide 10: Safety and permissions
- **Title:** Connectors are permission-aware
- **Content:** Three key principles with icons:
  1. **Scoped access** — Each connector only gets access to what you approve
  2. **Least privilege** — Grant the minimum permissions needed for the task
  3. **User control** — You confirm sensitive actions before Claude executes them
- **Speaker notes:** This is important and I don't want to skip it. Connectors are designed with safety in mind. Three principles. First, scoped access — when you enable a connector, you choose what it can see. A Notion connector doesn't automatically get access to your entire workspace; you scope it to specific pages or databases. Second, least privilege — only grant the permissions the connector actually needs. If Claude only needs to read tickets, don't give it write access. Third, user control — for sensitive actions like deleting something or posting publicly, Claude asks for confirmation before executing. You stay in the loop. This ties back to the CLAUDE.md conversation from last month — your project context files can include rules about what connectors are allowed to do.

### Slide 11: Getting started
- **Title:** Try it this week
- **Content:** Three steps:
  1. **Claude.ai / Desktop:** Open Settings > Connectors > browse the directory > toggle on
  2. **Claude Code:** Add connectors to your project's `.claude/settings.json` or user settings
  3. **Custom:** Build a connector for an internal tool using the MCP SDK
- **Speaker notes:** Here's how to actually get started. If you're on Claude.ai or Desktop, it's just a settings toggle — browse the directory, find the connector you want, turn it on, authorize it. In Claude Code, you add connector configuration to your settings file — this can be per-project or global. And if you want to connect Claude to something internal that doesn't have a pre-built connector, you can build one with the MCP SDK. We can dig into that in a future session if there's interest. I'd encourage everyone to try connecting at least one tool this week.

### Slide 12: What's next
- **Title:** Coming up in the series
- **Content:**
  - **June (Session 4):** How Standard Co built a Claude Agent for customer success — humans in the loop
  - **July (Session 5):** GitHub workflow + deployments + release notes
  - **August (Session 6):** Chrome extension + AWS/Azure + sharing context
- **Speaker notes:** Next month we're going to take everything we've learned — Claude Code, project context, connectors — and look at how Standard Co actually built a Claude Agent for customer success while keeping humans in the loop. That'll be a real case study from our own work. Then in July we'll cover the GitHub/deployment workflow, and in August we'll wrap up with the Chrome extension, cloud integrations, and sharing context across a team. Questions?

### Slide 13: Q&A
- **Title:** Questions?
- **Content:** Minimal — maybe the Standard Co logo or series branding
- **Speaker notes:** Open the floor for questions. Common topics that might come up: security/data privacy with connectors, which connectors are most useful to start with, how custom connectors work, cost implications, differences between connectors in Claude.ai vs Claude Code.

---

## Style notes
- Keep slides visually clean — avoid walls of text
- Use diagrams and icons where possible (especially slides 3, 4, 5, 6)
- The two demo slides (8, 9) should be minimal since the presenter will be screen-sharing
- Match the style and formatting of the previous two sessions in this series if possible
- Total: 13 slides for a 45-minute session (roughly 3–4 min per slide, with the two demos taking the bulk of time)
