# zenith-landing

A single, self-contained static landing page that hosts Zenith's shutdown message.
No build step, no framework, no runtime dependencies, and no service that requires an
ongoing subscription — just a domain and free static hosting.

## What's here

| File | Purpose |
| --- | --- |
| `index.html` | The entire page. Inline CSS, inline SVG logo, zero external requests. |
| `404.html` | Redirects any unknown path back to `/` so every URL shows the message. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (no Jekyll processing). |

## Editing the message

The copy lives directly in `index.html` under the `MESSAGE FROM ABIGAIL` comment block.
Each paragraph is its own `<p>` tag. Search the file for `TODO` to find the spots that
still need real values:

- The message body (currently tasteful placeholder copy).
- The contact email (`hello@example.com`).

## Branding notes

Colors and logo are pulled from Zenith's brand system (burgundy `#530D11` on cream
`#F7F4EC`, with the official brandmark + wordmark inlined as SVG).

The brand fonts (Self Modern, Suisse Intl) are **commercially licensed** and are
deliberately **not** shipped here, since this is a public repo. The page falls back to a
Georgia serif for display and a system sans for body, preserving the serif-display /
sans-body relationship.

## Hosting (GitHub Pages)

1. Push this repo to `zenithhealth`.
2. **Settings → Pages →** Source: *Deploy from a branch*, Branch: `main` / `root`.
3. To serve the custom domain, add it under **Settings → Pages → Custom domain**
   (GitHub will create/commit a `CNAME` file), then point the domain's DNS at GitHub
   Pages. The domain is paid through 2027.

## Local preview

Open `index.html` directly in a browser, or:

```sh
python3 -m http.server 8000   # then visit http://localhost:8000
```
