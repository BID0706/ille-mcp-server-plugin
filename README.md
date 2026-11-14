# ILLE MCP Server

A WordPress plugin that exposes a native **MCP (Model Context Protocol) server**, so AI assistants — Claude Desktop, Cursor, ChatGPT, Grok, and any MCP-compatible client — can create, review, and publish posts on a WordPress site without Node.js or a separate MCP gateway.

This repository is the standalone **MCP server** plugin, split out of [ILLE Post Generator V2](https://github.com/BID0706/wordpress-automated-posting). The post-generation admin UI lives in a separate plugin repository.

> **Status:** repository scaffold. The plugin code is being extracted; this branch currently contains project scaffolding only.

## Planned capabilities

- **MCP endpoint** — `POST /wp-json/ille/v2/mcp`, MCP Streamable HTTP transport (JSON-RPC 2.0).
- **Authentication** — per-user API keys (`X-API-Key`), OAuth 2.0 Bearer tokens (built-in or external mode), WordPress sessions, role allow-lists, and auth-failure throttling.
- **Content tools** — `generate_post`, `create_post`, `get_drafts`, `publish_post`, `upload_image`.
- **Server tools** — endpoint info, API-key management, allowed roles, model and prompt configuration, schedules, and activity-log access.
- **Admin settings** — MCP server, authentication, API keys, OAuth clients, and model configuration for the headless server.

## Branches

| Branch  | Purpose |
|---------|---------|
| `main`  | Stable, production-ready code |
| `stage` | Pre-release / staging integration |

Public visitors have **read-only access**: anyone may clone or download the repository, but only maintainers can push.

## Requirements (planned)

- WordPress 6.0+
- PHP 8.1+
- At least one supported AI provider key (Google Gemini, OpenAI, or xAI)
- [Yoast SEO](https://yoast.com/wordpress/plugins/seo/) (optional, for SEO metadata integration)

## Installation (planned)

1. Clone the repository into `wp-content/plugins/`:
   ```bash
   git clone https://github.com/BID0706/ille-mcp-server-plugin.git
   ```
2. Activate **ILLE MCP Server** in **Plugins**.
3. Open the plugin settings and configure an AI model key and API access.

## Clone

```bash
git clone https://github.com/BID0706/ille-mcp-server-plugin.git
# staging branch
git clone --branch stage https://github.com/BID0706/ille-mcp-server-plugin.git
```

## License

GPL-2.0-or-later. See [LICENSE](LICENSE).
