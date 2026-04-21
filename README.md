# sollu.io — marketing site

Static site for [sollu.io](https://sollu.io). Single `index.html` + `assets/`. No build step.

## Deploy (GitHub Pages)

1. Push this folder to a public GitHub repo (e.g. `sollu-site`).
2. Repo → **Settings** → **Pages** → Source: **Deploy from a branch** → Branch: `main`, folder: `/ (root)` → Save.
3. Wait ~60 seconds. Site is live at `https://<username>.github.io/<repo>/`.

## Custom domain (sollu.io)

The `CNAME` file in this repo points Pages at `sollu.io`. At your DNS registrar, add:

**Apex (`sollu.io`)** — four A records:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**www (`www.sollu.io`)** — one CNAME:

```
<your-username>.github.io
```

After DNS propagates (5–60 min), tick **Enforce HTTPS** on the Pages settings page.

## Local preview

Just open `index.html` in a browser, or:

```
python3 -m http.server 8000
```

## Editing

All copy, styles, and JS are in `index.html`. Brand SVGs are in `assets/`.
