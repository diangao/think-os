# MCP Protocol

> Building tools with Model Context Protocol

---

## What is MCP?

Protocol for connecting LLMs to external data and tools. Anthropic's standard for extending Claude.

## Current Project: Research Assistant

Building an MCP server that can:
- Search my notes and documents
- Fetch and summarize web content
- Track topics I'm learning about

### Progress

- [x] Set up basic MCP server structure
- [x] Implement file search tool
- [ ] Add web scraping capability
- [ ] Build conversation memory

### Architecture

```
User Query → Claude → MCP Server → Tools
                ↑           ↓
                └── Results ──┘
```

## Learnings

- MCP makes it easy to give Claude custom tools
- Need to be thoughtful about prompt design for tool use
- State management is tricky (stateless tools vs stateful server)

## Resources

- MCP docs: https://modelcontextprotocol.io
- Example servers: https://github.com/modelcontextprotocol
- Anthropic cookbook

---
