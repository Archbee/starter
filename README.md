<div align="center">
  <a href="https://archbee.com">
    <img src="https://archbee.com/archbee-logo.svg" alt="Archbee" height="64" />
  </a>
  <h3>Archbee Starter</h3>
  <p>The starter kit for your Archbee docs — clone, customize, and preview locally.</p>
</div>

---

## Getting Started

### 1. Clone this repo

Click **"Use this template"** above, or clone directly:

```bash
git clone https://github.com/Archbee/starter.git my-docs
cd my-docs
```

### 2. Install the CLI

```bash
npm install -g @archbee/cli
```

### 3. Preview locally

```bash
archbee dev
```

Your docs are live at `http://localhost:3000` with hot reload.

## What's Included

This starter comes with two spaces and example content covering every Archbee block:

**Documentation space** — guides for getting started, configuration, navigation, markdown, theming, branding, and API commands.

**Blocks space** — live examples of every block type organized by category:

- **Basic** — Headings, Expandable Headings, Lists, Tables, Button, Callout, Horizontal Divider, Vertical Split, Blockquote, Link Grid, Workflow, Tabs
- **Media** — File, Image, YouTube or Vimeo
- **Developer** — Code Editor, Code Drawer, Mermaid Diagram, TeX, API Endpoint, Changelog

Four built-in templates: **Stripe**, **ColorNav**, **Windy**, **Booklet**. Set via `"template"` in `archbee.json`.

## Project Structure

```
my-docs/
├── archbee.json           ← Configuration (name, template, colors, navigation)
├── guides/                ← Documentation space
│   ├── index.mdx          ← Home page
│   ├── quickstart.mdx
│   ├── essentials/        ← Configuration, navigation, markdown, code, images
│   ├── customization/     ← Templates, theming, branding
│   └── api/               ← API command reference
├── blocks/                ← Blocks showcase space
│   ├── headings.mdx
│   ├── callouts.mdx
│   ├── code-drawers.mdx
│   └── ... (21 block pages)
└── public/                ← Static assets (logos, favicon)
```

## Development

| Command | Description |
|---------|-------------|
| `archbee dev` | Start local preview with hot reload |
| `archbee validate` | Check config and doc structure for errors |
| `archbee broken-links` | Find broken internal links |
| `archbee dev --port 3001` | Use a different port |

Edit any `.mdx` file and the browser updates instantly. Changes to `archbee.json` (colors, navigation, template) also reload in real time.

## Configuration

All settings live in `archbee.json`. Key fields:

```json
{
  "name": "My Docs",
  "template": "stripe",
  "hostingColor": "#2166AE",
  "docsPath": "guides",
  "structure": { "docsTree": [...] },
  "sites": [{ "name": "Blocks", "docsPath": "blocks", ... }]
}
```

## Compatible Projects

The CLI auto-detects your project format — drop into any existing project and run `archbee dev`:

- `archbee.json` — native Archbee config
- `docusaurus.config.js` / `.ts` — Docusaurus projects

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Config not found | Make sure `archbee.json` is in the project root |
| Port in use | The CLI auto-tries the next available port |
| Outdated CLI | Run `archbee update` |
| Node.js required | Install Node.js 18+ from [nodejs.org](https://nodejs.org) |

## Learn More

- [Archbee Documentation](https://www.archbee.com/docs)
- [Archbee CLI on npm](https://www.npmjs.com/package/@archbee/cli)
- [Archbee Website](https://archbee.com)
