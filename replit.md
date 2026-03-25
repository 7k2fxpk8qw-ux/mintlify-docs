# Running Mintlify Docs on Replit

This repository is a **Mintlify Starter Kit** for building and previewing documentation sites.

## Setup

1. **Create a new Repl** — choose the **Node.js** template when importing this repository.

2. **Install dependencies** (if prompted or if `node_modules` is missing):
   ```bash
   npm i
   ```

3. **Run the Mintlify CLI**:

   Using `npx` (recommended in Replit to avoid global install issues):
   ```bash
   npx mint dev
   ```

   Or install globally first, then run:
   ```bash
   npm i -g mint
   mint dev
   ```

4. **View your docs** — Replit exposes port `3000` in the built-in webview. The preview will be available at `http://localhost:3000` (or via the Replit webview URL).

## Configuration

The main config file is **`docs.json`** and must be present at the **repository root**. It controls your site name, navigation, colors, and more.

## Publishing

To deploy your docs publicly:

1. Install the [Mintlify GitHub App](https://dashboard.mintlify.com/settings/organization/github-app) from your Mintlify dashboard.
2. Connect it to this repository.
3. Push changes to your default branch — Mintlify will automatically deploy them to production.

## Troubleshooting

- If the dev server doesn't start, run `npx mint update` to get the latest CLI version.
- If a page shows a 404, make sure `docs.json` is at the repo root and the page path is listed in the `navigation` section.
