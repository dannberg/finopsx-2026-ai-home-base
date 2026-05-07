# Vendor Contracts

A place to keep your executed vendor agreements alongside the rest of your AI Home Base, so your agent can reference them when the conversation calls for it.

## Why this folder exists

A FinOps practitioner's workday touches contracts constantly — renewal prep, invoice reconciliation, commitment utilization questions, "when does this auto-renew," "what's our walk-away leverage." Most of the time those answers live in a PDF buried somewhere in Drive that nobody's read since signing.

Keeping the actual documents inside your AI Home Base means your agent can read them on demand. A few examples of what that unlocks:

- *"Draft the renewal brief for Datadog"* — the agent reads the current contract, pulls term, commitment, and pricing, and starts the draft with real numbers instead of placeholders.
- *"Is this Snowflake invoice line correct?"* — the agent compares the invoice to the rate card in the order form.
- *"What's our walk-away leverage on the GCP renewal?"* — the agent surfaces the relevant termination, ramp, and commitment-flexibility terms.

This folder pairs especially well with the [`renewal-prep`](../../Skills/) and [`commitment-utilization-check`](../../Skills/commitment-utilization-check/SKILL.md) skills.

## What to put here

- Executed Master Service Agreements (MSAs)
- Order forms, amendments, and SOWs
- Pricing schedules and rate cards
- Renewal notices and termination letters
- Markdown summaries of any of the above

PDFs are fine. Markdown summaries of the key terms are even better — your agent will work faster and more accurately against a structured summary than against a 60-page legal PDF. A reasonable pattern: drop the PDF in, then ask the agent to produce a `<vendor>-summary.md` next to it the first time you reference it, and keep both.

## Don't commit these to a public repo

Vendor contracts are almost always confidential. If your AI Home Base lives in a public Git repo (as the one this README is in does), do **not** put real contracts here. Either:

- Keep your AI Home Base private, **or**
- Use a `.gitignore` rule that excludes the contents of this folder while keeping the README, e.g.:

  ```gitignore
  Reference/Vendor Contracts/*
  !Reference/Vendor Contracts/README.md
  ```

The folder in *this* repo is intentionally empty — it's a structural placeholder showing where the contracts would go in your own copy.

## A note on legal sensitivity

For contracts with active disputes or in-flight negotiations, your own internal AI agents may not be the right place to store them either. Check with your legal team when in doubt. The default should be: keep it out unless you've confirmed it's safe to include.
