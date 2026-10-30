# Mintlify Starter Kit

Use the starter kit to get your docs deployed and ready to customize.

Click the green **Use this template** button at the top of this repo to copy the Mintlify starter kit. The starter kit contains examples with

- Guide pages
- Navigation
- Customizations
- API reference pages
- Use of popular components

**[Follow the full quickstart guide](https://starter.mintlify.com/quickstart)**

## AI-assisted writing

Set up your AI coding tool to work with Mintlify:

```bash
npx skills add https://mintlify.com/docs
```

This command installs Mintlify's documentation skill for your configured AI tools like Claude Code, Cursor, Windsurf, and others. The skill includes component reference, writing standards, and workflow guidance.

See the [AI tools guides](/ai-tools) for tool-specific setup.

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Mintlify's GitHub app deploys `main` to docs.lattica.finance (custom domain; the DNS record is managed in `latticafi/platform`) and lattica.mintlify.app. `ci.yml` runs `pnpm check` (`mint validate` and `mint broken-links`) on pull requests and pushes to `main`; run `pnpm install && pnpm check` locally before pushing.

Mintlify serves PDFs only on Enterprise plans, so the whitepapers live on the landing site (`latticafi/landing-page`, `https://lattica.finance/<file>.pdf`). The `redirects` in `docs.json` keep the old `docs.lattica.finance/<file>.pdf` links working.

## Need help?

### Troubleshooting

- If your dev environment isn't running: Run `mint update` to ensure you have the most recent version of the CLI.
- If a page loads as a 404: Make sure you are running in a folder with a valid `docs.json`.

### Resources
- [Mintlify documentation](https://mintlify.com/docs)
