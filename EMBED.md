# Embedding (Squarespace Code Block)

Add a **Code Block** in Squarespace, set it to HTML, and paste the snippet below. Replace the placeholder URL with your Pages URL.

```html
<div style="position:relative;width:100%;aspect-ratio:16/10;min-height:420px;max-height:85vh;">
  <iframe
    src="https://<user>.github.io/<repo>/?embed=1"
    title="Beehive thermal simulation – 3D viewer"
    style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:8px;"
    loading="lazy"
    allow="fullscreen"
    allowfullscreen></iframe>
</div>
<p style="font-size:12px"><a href="https://<user>.github.io/<repo>/" target="_blank" rel="noopener">Open full viewer ↗</a></p>
```

Notes:
- **Responsive height:** the wrapper keeps a 16:10 box with a 420 px minimum and caps it at 85 % of the viewport height. Adjust `aspect-ratio` to taste; on phones try `aspect-ratio:3/4`.
- **Embed mode:** `?embed=1` hides the side panels and charts. The ☰ button opens the controls and ⛶ goes full screen; this needs `allowfullscreen`.
- **Framing:** GitHub Pages sends no `X-Frame-Options` or `frame-ancestors` header, and the page sets none, so it can be framed.
- **Other parameters** you can append: `&run=24h_Edmonton_CA_Jan` (the winter day) and `&k=<step>`.
- Squarespace Code Blocks with iframes need a Business plan or higher on some Squarespace versions.
