# Lucas Faninger – portfolio

A 2-minute tour of my career as a top-down pixel-art game, in French, German and English.
Plain HTML, CSS and JavaScript (Canvas 2D), no build step and no game engine.

## Files

| File | Role |
|---|---|
| `index.html` | The whole site: game, texts (FR/DE/EN), text version, PDF CV export |
| `og-image.png` | Share preview image (LinkedIn, Teams, e-mail) |
| `staticwebapp.config.json` | Azure Static Web Apps settings |

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Settings to fill in `index.html`

Near the top of the `<script>`:

- `LINKEDIN`: LinkedIn profile URL (already set)
- `LOOKING_FOR`: what I'm looking for, a few lines per language (`fr`, `de`, `en`)
- `SITE_URL`: public address, printed in the PDF CV footer
- `GOATCOUNTER`: GoatCounter code (set to `lucasfaninger`)

In the `<head>`, replace `og-image.png` in the `og:image` tag with the full URL
(for example `https://my-domain/og-image.png`): LinkedIn needs an absolute URL.

## Deploy (Azure Static Web Apps)

1. Push this folder to a GitHub repository.
2. In the Azure portal, create a **Static Web App** linked to the repository.
   Build preset: **Custom**, app location `/`, no API, no output location.
3. Azure adds a GitHub Actions workflow; every push to `main` redeploys the site.
4. Add your domain under **Custom domains**.

## Handy URL parameters

- `?night` / `?day`: force night or day mode
- Konami code (↑ ↑ ↓ ↓ ← → ← → B A): developer mode
