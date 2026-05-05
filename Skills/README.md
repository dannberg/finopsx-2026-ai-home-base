# Skills

Skills are reusable instructions that the AI loads automatically when triggered. Each skill is a directory with a `SKILL.md` file that tells the AI *when* to use it (the description) and *what to do* when invoked (the body).

This folder is a sample set, geared toward a FinOps practitioner. Treat them as starting points — fork, edit, swap in your org's specifics, and add your own.

## How a skill gets triggered

The AI reads the `description` field in each skill's frontmatter and picks the right one based on what you're working on. Good descriptions name the trigger phrases and the inputs the skill needs.

## Anatomy of a skill

```
skill-name/
├── SKILL.md          # required — frontmatter + instructions
├── templates/        # optional — output templates the skill references
├── scripts/          # optional — helper scripts (Python, bash, SQL)
└── reference/        # optional — org-specific context the skill needs
```

The frontmatter:

```yaml
---
name: skill-name
description: When to invoke this skill — the trigger conditions and inputs.
---
```

## Adding your own

1. Pick a kebab-case name (`tag-coverage-report`, not `Tag Coverage Report`)
2. Write the description as the trigger you want the AI to recognize, not a marketing blurb
3. In the body, say what inputs to confirm, what steps to take, and what the output should look like
4. If your team has house-style rules (always lead with dollar impact, no jargon, ticket-ready format), encode them in the skill — that's the whole point

## What's in this folder

| Skill | What it does |
|---|---|
| [anomaly-triage](anomaly-triage/SKILL.md) | Investigate a cost spike end-to-end and produce the stakeholder communications |
| [cost-spike-postmortem](cost-spike-postmortem/SKILL.md) | Standardized writeup for any anomaly that's been resolved |
| [monthly-business-review-prep](monthly-business-review-prep/SKILL.md) | Pulls last month's spend, computes trends, drafts the MBR narrative |
| [exec-digest](exec-digest/SKILL.md) | One-paragraph CFO-grade summary on any topic, in house style |
| [tag-coverage-report](tag-coverage-report/SKILL.md) | Per-tag compliance report plus the "please fix" Slack DMs to owners |
| [commitment-utilization-check](commitment-utilization-check/SKILL.md) | CUD/RI/SP utilization report with projected over- or under-use |
| [right-sizing-recommendations](right-sizing-recommendations/SKILL.md) | Ticket-ready right-sizing actions with dollar impact estimates |
| [prompt-library-manager](prompt-library-manager/SKILL.md) | When you discover a prompt that works, save it with metadata for next time |

## A note on org-specific data

These examples use placeholder values for table names, account IDs, label keys, and Slack channels. Search-and-replace before using:

- `gcp_billing_export.cost_data` — your billing export table
- `account_4421` etc. — your account IDs
- `#data-eng`, `#finops` — your channel names
- `cost_center`, `team`, `environment` — your tag keys
