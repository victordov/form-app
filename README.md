# Form website

Static website for Form, an iPhone app for keeping a personal record of a prescribed GLP-1 or peptide treatment. Served by GitHub Pages at https://victordov.github.io/form-app/.

Plain HTML and one stylesheet. No JavaScript, no build step, no external fonts, no analytics, no CDN.

## Pages

| Path | Page | Used as |
| --- | --- | --- |
| `index.html` | Overview | App Store Marketing URL |
| `support/` | Support | App Store Support URL |
| `privacy/` | Privacy Policy | App Store Privacy Policy URL, in-app link |
| `health-data/` | Consumer Health Data Privacy Policy | Washington MHMDA / Nevada SB 370 policy, linked from the homepage and every footer |
| `terms/` | Terms of Use | Subscription Terms of Use (EULA) link |
| `404.html` | Not found | GitHub Pages error page |

`style.css` holds the design tokens (light and dark) and all styles. `.nojekyll` turns off Jekyll processing.

## Links

This is a project site, so every link is relative (`privacy/`, `../terms/`). Don't start a link with `/`. The one exception is `404.html`, which sets `<base href="https://victordov.github.io/form-app/">` because GitHub Pages serves it at any depth. Update that line if the site moves to a custom domain.

## Preview locally

From the repository root:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000/.

## Publishing

In the repository settings, under Pages, deploy from the `main` branch, root folder.

## Updating a policy

1. Edit the page.
2. Change the "Last updated" date on that page (and "Effective" if the change takes effect on a new date).
3. The policies say changes are announced in the app or on the page itself, so add an in-app notice for material changes.
