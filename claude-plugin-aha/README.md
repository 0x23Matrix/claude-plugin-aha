# 💡 Aha — Capture Your Insights

A Claude Code plugin that helps you capture "aha moments" from AI conversations and build a personal knowledge network over time.

## The Problem

You're chatting with AI, working through a problem, and suddenly — *aha!* — you realize something that could have saved you hours last week. But by tomorrow, that insight is buried in conversation history, forgotten.

## What This Plugin Does

`/aha` extracts the insight from your conversation, writes it down in a structured format, categorizes it, and connects it to your previous learnings. Over time, you build a searchable, interconnected knowledge base of things you've actually learned — not bookmarks you'll never revisit.

## Install

```
/plugin install aha
```

## Usage

After a moment of realization in any conversation:

```
/aha
```

Or with a hint about what you learned:

```
/aha learned that retention rate matters more than DAU for subscription products
```

When your knowledge base grows and categories get messy, retag to unify them:

```
/aha retag
```

## What Gets Saved

Each insight is stored as a markdown file in `~/.claude/aha/entries/` with:

- **Insight** — The core realization, generalized as a principle
- **Context** — What you were working on when you discovered it
- **Details** — Supporting explanation, code snippets, examples
- **Related** — Links to your other insights on related topics

An `index.md` provides a chronological overview of all captured insights.

## The Knowledge Network

As your collection grows, insights automatically link to related entries — forming a personal knowledge graph. A user retention insight from January might connect to an onboarding insight from March, revealing patterns in how you think about product growth.

## Storage

```
~/.claude/aha/
├── index.md                          # Chronological index
└── entries/
    ├── 2026-01-15-retention-over-dau-for-subscriptions.md
    ├── 2026-01-22-user-onboarding-aha-moment-timing.md
    └── ...
```

All files are plain markdown — grep-friendly, version-controllable, yours forever.

## License

MIT
