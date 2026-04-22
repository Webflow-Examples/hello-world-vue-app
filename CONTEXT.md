# CONTEXT — hello-world-vue-app

Orientation for contributors to this **Vue 3 + Vite** Hello World example for
[Webflow Cloud](https://developers.webflow.com/webflow-cloud). Keep this file
current when structure or workflows change.

## What this is

A minimal, branded **Hello, world** page built with **Vue 3 + Vite** and
deployed on Cloudflare Workers via Webflow Cloud. This is the **vanilla**
variant (no bindings — UI only).

The page shows a Webflow brand hero, gradient logo, and curated doc cards
pointing at the Webflow Cloud documentation.

## Stack

- Framework: **Vue 3** on **Vite 6** (`<script setup lang="ts">`)
- Styling: Tailwind v3 + `wf-*` brand tokens (see `src/style.css`)
- Deploy target: Cloudflare Workers via **Webflow Cloud** (static assets)

## Repo layout

```
index.html
src/
  App.vue                    ← page content, hero, DOC_LINKS
  main.ts                    ← Vue app bootstrap
  style.css                  ← Tailwind + .wf-* design tokens
  components/
    WebflowLogo.vue
    DocCard.vue
vite.config.ts
tailwind.config.js
tsconfig.json
package.json
```

## Running locally

```bash
npm install
npm run dev
```

## Building

```bash
npm run build             # vue-tsc -b && vite build
```

Build output lands in `dist/`.

## Editing the UI

- **Page content (hero, CTAs, doc cards):** `src/App.vue`
- **Doc card list:** search for `DOC_LINKS` in `src/App.vue`
- **Brand tokens and `.wf-*` styles:** `src/style.css`
- **`<head>` (title, favicon, theme-color):** `index.html`

## Deploying to Webflow Cloud

1. Push this repo to GitHub.
2. In your Webflow Cloud project, connect the repo and pick a mount path
   (e.g. `/my-app`). The app runs under any prefix.
3. Webflow Cloud builds with `npm run build` on deploy.

See [Deployments](https://developers.webflow.com/webflow-cloud/deployments)
and [Environments](https://developers.webflow.com/webflow-cloud/environments).

## Contributing

- Keep the **Webflow brand tone**: blue gradient (`#4353FF` → `#146EF5`), dark
  background, minimal copy. Reuse the existing `.wf-*` CSS tokens.
- This is a Hello World. Do **not** add extra pages, client-state libraries,
  or UI kits. Small and readable beats clever.
- Run `npm run build` before opening a PR.
- Keep **cross-app parity**: if you change shared copy or doc links, update
  the sibling `hello-world-*-app[-bindings]` apps too.

## Related docs

- [Webflow Cloud overview](https://developers.webflow.com/webflow-cloud)
- [Getting started](https://developers.webflow.com/webflow-cloud/getting-started)
- [Storing data (SQLite, KV, R2)](https://developers.webflow.com/webflow-cloud/storing-data/overview)
- [Environments](https://developers.webflow.com/webflow-cloud/environments)
- [Deployments](https://developers.webflow.com/webflow-cloud/deployments)
- [Configuration](https://developers.webflow.com/webflow-cloud/environment/configuration)
- [Limits](https://developers.webflow.com/webflow-cloud/limits)
