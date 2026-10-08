# OIKOS

**Portfolio Design Operating System**

This repository contains the current OIKOS desktop conversation surface. MCP is an implementation capability underneath the product, not the product identity.

## Product surface
- One shared question, shown once
- Six core model participants, with 5-person and 15-person group modes
- Choose who you listen to, or listen to everyone
- Add people/roles such as Chairman, Scribe, Risk, Finance, Customer and Researcher
- Chairman synthesis
- Live action capture
- Timer/alarm controls
- Scratch pad
- Markdown, JSON and clipboard export
- Document/transcript/CSV/JSON/text import
- OIKOS branding and light portfolio-workspace treatment
- Runtime state and receipts surfaced as REAL/DEGRADED
- Model discovery from the live Universal Chat runtime, while preferring exact configured model IDs

## Persistence
The OIKOS front end sends turns to the existing T4H Universal Chat Cloudflare Worker. That runtime persists conversation messages, executions and receipts in the Supabase conversation/runtime stores. The browser also keeps the BYOK token in session storage only.

The important distinction is:
- Conversation data: persisted server-side through the Universal Chat runtime/Supabase path.
- BYOK token: browser session only.
- Current UI: maintains the active group state in the browser; conversation reload/history browsing is a subsequent surface.

## Runtime
Live front end: https://tech4humanity-002.github.io/mcp-desktop/

Universal Chat runtime: https://t4h-universal-chat.troy-latter.workers.dev/

## Acceptance already established
- GitHub Pages front end previously returned HTTP 200.
- Universal Chat health endpoint previously returned HTTP 200.
- CORS from the GitHub Pages origin was confirmed.
- A live model stream previously returned a REAL receipt, conversation ID and execution ID.

## Current boundary
BYOK is currently OpenRouter/session based, not generic provider OAuth. Plugin/automation navigation is a product surface; actual execution remains dependent on the underlying capability/runtime being wired.