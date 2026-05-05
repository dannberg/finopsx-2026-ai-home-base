# AI Home Base — FinOps X 2026

A public companion repo for the FinOps X 2026 talk *AI for FinOps: From Hype to Helpful* by [Dann Berg](https://github.com/dannberg) (Squarespace).

This is an example of an "AI Home Base" — the folder structure, prompts, and skills I actually use in my day-to-day FinOps work. It's published here so the audience can fork it and use it as a starting point for their own.

## What's in here

| Folder | What it is |
|---|---|
| [Prompts/](Prompts/) | The doctored prompts from the talk's "Real Use Cases" section. Drop-in templates for SQL queries, anomaly communications, policy drafts, and architecture review. |
| [Skills/](Skills/) | Reusable skill definitions an AI assistant can invoke automatically. Each one captures a workflow with house-style rules baked in. |
| [Reference/](Reference/) | Personal config and dotfiles I demoed during the talk. |

## How to use it

1. Fork the repo (or just copy the structure).
2. Search-and-replace placeholder values — table names, account IDs, channel names, tag keys — for your own org.
3. Plug it into your AI tool of choice. Anything that supports loading skills (Claude, Cursor, etc.) will pick up the `Skills/` folder. Prompts can be pasted into any chat tool.

## Caveats

These are starting points, not best practices. They reflect my org's specifics, my preferences, and my model-version-of-the-week. Treat them like any other config — borrow what's useful, throw out what isn't, and update as the underlying tools shift.

## Talk

[Recording link will go here once published by the FinOps Foundation.]
