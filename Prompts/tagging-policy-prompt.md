I need to draft a GCP resource tagging policy for our org. Context:

- We're at Walk-stage FinOps maturity; current tagging compliance is ~60%.
- Required tags need to support cost center allocation, environment
  separation (prod/staging/dev), and team ownership for on-call routing.
- Infra is ~80% Terraform-managed; the rest is manually created in the
  Console (mostly engineering experimentation).
- Engineering culture is anti-bureaucracy. Any policy that doesn't
  explain WHY each tag is required will get rejected on review.

Draft a policy that includes:
1. Required tag keys with allowed values (or "free-form, follows
   naming convention X")
2. One-sentence business rationale per tag
3. Enforcement model: what's blocked at deploy time vs. flagged for
   review vs. tolerated
4. Phased rollout: what's enforced day 1 vs. month 3 vs. month 6
5. Exception process for teams that legitimately need to bypass

Tone: direct, engineering-friendly, no corporate-speak.
