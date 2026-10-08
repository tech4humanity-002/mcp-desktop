MCP Desktop

A clean multi-model conversation workspace derived from the MCP Desktop thread.

Product
- One conversation surface
- Multiple model panes
- Broadcast one prompt to multiple models
- BYOK OpenRouter token held in browser session
- Drag/drop text, Markdown, CSV and JSON for extraction/summarisation
- Conversation starters for common team patterns
- Workspace, model/token, plugin, instructions/recipe and automation entry points
- OIKOS presentation and T4H droid favicon

Runtime
The static front end is published on GitHub Pages and calls the existing T4H Universal Chat Cloudflare Worker for model execution.

Live: https://tech4humanity-002.github.io/mcp-desktop/
Runtime: https://t4h-universal-chat.troy-latter.workers.dev/

Acceptance
- GitHub Pages status: built
- Front end HTTP: 200
- Universal Chat health: HTTP 200
- Cross-origin API access from GitHub Pages origin: confirmed
- Live stream acceptance receipt: 49b6c1bf-b962-40bd-8ef2-bb634ba1cd1c
- Conversation ID: 9e85c1bd-129b-40b9-bb48-03323c2fa965
- Execution ID: 4a2be907-1f6e-40a2-98f6-863b4060fb18

Important boundary
The current account connection is BYOK/session based, not a provider OAuth login. Plugin and automation controls are currently product-surface controls; their execution is not yet wired into this front end.
