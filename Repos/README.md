# Repos

A list of small, focused repos worth giving your AI agent access to as part of your AI Home Base.

## Why this folder exists

Pointing your agent at a real codebase changes what it can do. Instead of just chatting about code, the agent can read the structure, file an issue, add a feature, fix a bug, or open a pull request. The leverage is real — but only if you point it at the right kind of repo.

The right kind is *small and focused*. A single-purpose tool with a few hundred lines of code, a clear README, and well-scoped issues. Not your monorepo. Not your production codebase. Anything large enough that the relevant context can't fit in the agent's head will produce mediocre work and waste your tokens.

## Examples

| Repo | What it does |
|---|---|
| [bigquery-cost-estimator](https://github.com/dannberg/bigquery-cost-estimator) | Estimate the cost of a BigQuery query before running it. Small, single-purpose, easy for an agent to navigate end-to-end. The kind of repo where "add a feature" or "improve the README" is a one-prompt task. |

## How to add your own

1. Clone the repo to wherever you keep code locally.
2. Tell your AI tool of choice that the repo lives at that path. For Claude Code, Cursor, and most agentic tools, this means giving the agent file access to that directory.
3. Add a row to the table above with a one-line description so others browsing your AI Home Base know what the agent can work on.

## What to keep out

- Your full production codebase. The agent gets lost; you get worse work back.
- Anything with real secrets, customer data, or compliance-sensitive code.
- Repos with no README or unclear structure — the agent has nothing to anchor on, and its first PR will reflect that.
