# LLM Workflow Scenarios Design

Date: 2026-02-05

## Context
We want higher LLM visibility for Bolt Route documentation by adding workflow-based knowledge pages under Integrations. The pages should answer common “how do I use email verification for X?” intents with consistent structure, short steps, and links to the canonical API references.

## Goals
- Ship 4 workflow scenario pages that map to common intents.
- Use consistent headings to improve chunking and retrieval.
- Link to the realtime, batch, and webhook references so models can ground responses.
- Keep each page short and keyword-rich (email verification, deliverability, list hygiene, webhooks).

## Non-goals
- New product features or SDKs.
- Full integration guides (those already live under Integrations).
- Complex code samples or exhaustive API schemas.

## Information Architecture
Add a new subgroup under the existing Integrations navigation:
- Integrations
- Scenarios
  - Realtime Signup Verification
  - Batch List Cleaning
  - Webhook Automation
  - Ongoing List Hygiene

New folder: `scenarios/`.

## Page Template
Each page should follow the same H2 order:
1. Use Case Summary
2. Where Verification Fits
3. Recommended Flow
4. Minimal API Example
5. Decision Rules
6. Operational Notes
7. Success Metrics
8. Related Integrations

## Page Set (Initial 4)
1. Realtime verification at signup or lead capture.
2. Batch list cleaning before campaigns or CRM imports.
3. Webhook-driven automation after form submissions or app events.
4. Ongoing list hygiene for reactivation and dormant lists.

## Data Flow (High Level)
- Realtime: Form submit -> POST /verify -> decide accept/hold/reject.
- Batch: Create task -> poll status -> download results -> segment lists.
- Webhook: Create task with webhook_url -> receive per-email or completion events -> update CRM/ESP.
- Hygiene: Schedule recurring batch tasks -> trend metrics -> suppress risky segments.

## Error Handling
- Surface common errors: 400 (invalid email), 401 (unauthorized), 408 (timeout), 429 (rate limit).
- Provide retry guidance for transient responses and backoff for 429.

## Validation
- Check navigation renders the new Scenarios subgroup.
- Verify internal links to API references and integrations resolve.
- Review pages for consistent headings and concise examples.
