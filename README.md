# fomo-researcher

Multi-source research agent for Claude Code that investigates topics across GitHub, Reddit, Twitter, LinkedIn, and web.

## Features

- **Sequential multi-source research**: GitHub → Reddit → Twitter → LinkedIn → Web
- **Semantic duplicate detection**: Checks existing reports by content similarity, not just filename
- **Structured output**: Findings files + synthesized report with sentiment analysis
- **MCP integration**: Uses Brave Search, Context7, and GitHub MCP servers

## Installation

```bash
/plugin marketplace add razpetel/fomo-researcher
/plugin install fomo-researcher@razpetel
```

Then restart Claude Code.

## Usage

```
/research <topic | URL | image-path>
```

**Examples:**
- `/research Mem0 memory layer`
- `/research https://github.com/anthropics/claude-code`
- `/research screenshot.png`

**Skip for:** Simple facts, definitions, quick lookups — Claude will answer directly.

## What It Researches

| Source | What It Finds |
|--------|---------------|
| GitHub | Repository health, issues, PRs, activity |
| Reddit | Community sentiment, discussions (past year) |
| Twitter | Real-time buzz, influencer opinions (past month) |
| LinkedIn | Professional adoption signals |
| Web | News, docs, comparisons, Context7 library docs |

## Output

1. **Findings files** in `.claude/research-cache/<session>/`
2. **Synthesized report** in `research/catalogue/<date>-<slug>.md`
3. **Catalogue entry** in `research/catalogue.md`

## Requirements

This plugin works best with these MCP servers configured:
- Brave Search MCP (for Reddit, Twitter, web, news)
- GitHub MCP (for repository analysis)
- Context7 MCP (for library documentation)

## License

MIT
