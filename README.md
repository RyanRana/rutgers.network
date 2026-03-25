# rutgers.network landing site

Static site for `rutgers.network` with:

- Main page: `code.html`
- Application page: `apply.html`

## Deploy (Vercel)

1. Push this folder to GitHub.
2. Import the repo in Vercel.
3. Deploy with default static settings.

`vercel.json` is included so:

- `/` serves `code.html`
- `/apply` serves `apply.html`

## Analytics + Performance

Both pages include:

- Vercel Web Analytics (`/_vercel/insights/script.js`)
- Vercel Speed Insights (`/_vercel/speed-insights/script.js`)

These automatically report metrics once deployed on Vercel.
