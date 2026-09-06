# personal-site

The source for [dhruverrla.me](https://dhruverrla.me).

Hand-written HTML and CSS. No framework, no build step, no dependencies. What is in this
repository is exactly what ships — GitHub Pages serves these files as they sit.

## Files

| File | What it is |
|---|---|
| `index.html` | Landing page: experience, projects, the AvePoint pitch, education, contact |
| `outreach-engine.html` | Deep dive — architecture, four design decisions, known gaps |
| `banktracker.html` | Deep dive — the cycle-ahead rule, the JSON state model, the validator |
| `salt-creek.html` | Deep dive — sector screening method. No client data, by design |
| `styles.css` | One stylesheet. All design tokens are the `:root` block at the top |
| `CNAME` | The custom domain. Do not delete — Pages needs it |
| `.nojekyll` | Stops GitHub from running Jekyll over the files |
| `assets/` | The résumé PDF |

## Editing

Change the colors or type in one place: the `:root` block at the top of `styles.css`.
The dark palette is the `@media (prefers-color-scheme: dark)` block directly below it and
redefines the same token names — if you add a token, add it to both.

The architecture diagram on the outreach-engine page is inline SVG using the same tokens,
so it inverts with the theme. There is no image file to regenerate.

## Preview locally

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploying

Push to `main`. GitHub Pages redeploys automatically; it usually takes under a minute.

## Ground rules for what goes on this site

- No street address, no phone number. Email and LinkedIn only.
- Nothing about HelmIQ's product surfaces, clients, or specific defects — stack and process
  only.
- No Salt Creek company names, batch data, tracker rows, or screenshots.
- Never link the private `Banking-Outreach` repository. `outreach-engine` is its sanitized
  public twin and is the one to show.
