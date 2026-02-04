# Bolt Route Email Verification Docs

Source for the public documentation at [docs.boltroute.ai](https://docs.boltroute.ai).

Quick links:
- Docs: [docs.boltroute.ai](https://docs.boltroute.ai)
- Dashboard: [dashboard.boltroute.ai](https://dashboard.boltroute.ai)
- Support: [support@boltroute.ai](mailto:support@boltroute.ai)

**Quick start**

Install the Mintlify CLI:

```bash
npm i -g mint
```

Start the local preview server from the repo root:

```bash
mint dev
```

Open `http://localhost:3000`.

**Local development**

- Navigation and site config live in `docs.json`.
- Content lives in MDX files with frontmatter `title` and `description`.
- New pages must be added to `docs.json` to appear in navigation.

Content map:
- `guides/` for guidance and announcements
- `integrations/` for tool integrations
- `api-reference/` for API endpoint docs
- `snippets/` for reusable MDX fragments

**Deploy**

Production is managed by the Mintlify GitHub app. Install it from the [dashboard](https://dashboard.mintlify.com/settings/organization/github-app). Changes to the default branch deploy automatically.

**Contributing**

1. Create a branch.
2. Make MDX updates and preview with `mint dev`.
3. Open a PR.

**Content guidelines**

- Use clear, task‑oriented headings.
- Keep paragraphs short and use lists for steps.
- Avoid marketing language in how‑to pages.
- Include `title` and `description` frontmatter on every page.

**Support**

Email [support@boltroute.ai](mailto:support@boltroute.ai) for help.
