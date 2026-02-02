# fomo-researcher

> Because scrolling through 47 browser tabs at 2am to figure out if that new AI tool is legit... is not a personality trait.

**fomo-researcher** is a Claude Code plugin that does the obsessive research you'd do anyway — just faster, more thorough, and without the existential dread.

## The Problem

You hear about a new tool. You *need* to know:
- Is it actually good or just good at marketing?
- What does Reddit *really* think? (not the launch day hype)
- Is the GitHub repo alive or mass grave?
- Did that one Twitter person you trust say anything?
- Is anyone actually using this in production?

So you open 47 tabs. You forget why you opened half of them. Three hours later, you've learned more about the founder's college roommate than the actual product.

## The Solution

```
/research <topic>
```

That's it. Go touch grass. Come back to a comprehensive report.

## How It Works

```
                            /research "new shiny tool"
                                       │
                                       ▼
                        ┌──────────────────────────┐
                        │  📋 Check Catalogue      │
                        │  (semantic matching)     │
                        └────────────┬─────────────┘
                                     │
         ┌───────────┬───────────┬───┴───┬───────────┬───────────┐
         ▼           ▼           ▼       ▼           ▼           │
    ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐  │
    │ GitHub  │ │ Reddit  │ │ Twitter │ │LinkedIn │ │   Web   │  │
    │   MCP   │ │ (Brave) │ │ (Brave) │ │(Search) │ │ (All)   │  │
    └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘  │
         │           │           │           │           │       │
         │      ┌────┴────┐      │           │      ┌────┴────┐  │
         │      │ agent-  │      │           │      │ agent-  │  │
         │      │ browser │      │           │      │ browser │  │
         │      │(if deep)│      │           │      │(pricing)│  │
         │      └────┬────┘      │           │      └────┬────┘  │
         │           │           │           │           │       │
         └─────┬─────┴─────┬─────┴─────┬─────┴─────┬─────┘       │
               │           │           │           │             │
               ▼           ▼           ▼           ▼             │
         ┌─────────────────────────────────────────────┐         │
         │              🧠 Synthesis                    │◄────────┘
         │  Cross-reference • Themes • Sentiment       │  (prior research)
         └─────────────────────┬───────────────────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
        ┌──────────┐    ┌──────────┐    ┌──────────┐
        │  Report  │    │Catalogue │    │   Key    │
        │ (*.md)   │    │  Entry   │    │ Insights │
        └──────────┘    └──────────┘    └──────────┘
```

## What You Get

**One command. Five sources. Zero tab explosions.**

| Source | What It Digs Up |
|--------|-----------------|
| **GitHub** | Stars, forks, issue graveyard status, "last commit 2 years ago" warnings |
| **Reddit** | The *real* opinions (past year, not launch day astroturfing). Deep threads via agent-browser |
| **Twitter/X** | Influencer takes, mass hysteria levels, ratio alerts |
| **LinkedIn** | "Excited to announce" posts from people who actually shipped with it |
| **Web** | News, comparisons, pricing pages, Context7 docs. agent-browser for the juicy bits |

## Features

### Semantic Memory (Not Just Pattern Matching)

Already researched "Mem0"? Ask about "memory layer for AI agents" and it'll know they're related. No duplicate reports. No wasted tokens. It reads your research catalogue like a human would.

```
📋 Related reports: Mem0 (2026-02-02)
📄 Prior research: "Production-ready, 40K stars, YC-backed"
```

### Structured Output

Every research session produces:
- **Findings files** — Raw intel from each source
- **Synthesized report** — The "tl;dr but actually comprehensive" version
- **Sentiment analysis** — Is vibes good or vibes concerning?
- **Catalogue entry** — Searchable index of everything you've researched

### Works With Your MCP Stack

Plays nice with:
- **Brave Search** — Reddit, Twitter, news, web (the legal kind of scraping)
- **GitHub MCP** — Repo deep-dives without rate limit anxiety
- **Context7** — Library docs that are actually up-to-date
- **agent-browser** — When you need to actually *read* the page, not just find it

## Installation

```bash
/plugin marketplace add razpetel/fomo-researcher
/plugin install fomo-researcher@razpetel
```

Restart Claude Code. Research responsibly.

## Usage

```bash
# Tool/product research
/research Cursor IDE

# URL deep-dive
/research https://github.com/anthropics/claude-code

# "What is this screenshot of?"
/research screenshot.png

# The 3am spiral, but productive
/research "that memory thing everyone's talking about"
```

**Pro tip:** Skip `/research` for simple questions. Claude knows what a for-loop is. Save the big guns for actual research.

## Example Output

```markdown
# Mem0 Research Report

## Key Insights
- 40K+ GitHub stars, $24M Series A (YC-backed)
- +26% accuracy over OpenAI Memory in benchmarks
- Production-ready with hosted and self-hosted options

## Sentiment: Very Positive
The rare case where the hype matches reality...
```

## When NOT to Use

- "What's 2+2?" — Claude can handle this
- "Fix my code" — That's a different skill
- "Research my ex" — Sir, this is a Wendy's

## Requirements

For full functionality, configure these:
- **Brave Search MCP** — Web, Reddit, Twitter, news
- **GitHub MCP** — Repository analysis
- **Context7 MCP** — Library documentation
- **agent-browser** — Deep content extraction (pricing pages, long threads, comparison tables)

Works without them, just less comprehensive (like research without coffee).

## Why "FOMO"?

**F**ind **O**ut **M**ore **O**bsessively?

...okay fine, it's Fear Of Missing Out. Because you *will* miss out on good tools if you don't research them. And you *will* mass adopt bad tools if you only read the landing page. This plugin is the cure.

## License

MIT — Research freely, cite responsibly.

---

*Built for developers who mass open tabs and mass regret it.*
