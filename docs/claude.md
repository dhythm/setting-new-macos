# Claude

https://claude.ai/
https://claude.ai/download

## Claude Code

### MCP

```sh
claude mcp add playwright -s user npx @playwright/mcp@latest
claude mcp add o3 -s user \
	-e OPENAI_API_KEY=your-api-key \
	-e SEARCH_CONTEXT_SIZE=medium \
	-e REASONING_EFFORT=medium \
	-- npx o3-search-mcp
```
