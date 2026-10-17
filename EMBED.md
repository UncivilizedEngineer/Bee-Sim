# Embedding the Visualizer

You can embed the hive visualizer in other websites using an iframe. This is useful for integration with content management systems like Squarespace, WordPress, or custom HTML pages.

## Basic Embed Code

Replace `<your-pages-url>` with your actual GitHub Pages URL:

```html
<div style="position:relative;width:100%;aspect-ratio:16/10;min-height:420px;max-height:85vh;">
  <iframe
    src="<your-pages-url>/?embed=1"
    title="Beehive thermal simulation – 3D viewer"
    style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:8px;"
    loading="lazy"
    allow="fullscreen"
    allowfullscreen></iframe>
</div>
<p style="font-size:12px">
  <a href="<your-pages-url>/" target="_blank" rel="noopener">Open full viewer ↗</a>
</p>
```

## Embed Mode Features

The `?embed=1` parameter activates embed mode:
- Hides side panels and charts by default
- Shows only the 3D view and time controls
- Provides ☰ button to open control panel
- Supports full screen mode via ⛶ button

## Additional Parameters

Combine URL parameters with `&`:

- `&run=24h_Edmonton_CA_Jan` — select the winter day scenario
- `&k=<step>` — start at a specific time step

**Example:** `<your-pages-url>/?embed=1&run=24h_Edmonton_CA_Jan&k=72`

## Responsive Sizing

The wrapper div maintains a 16:10 aspect ratio with:
- Minimum height: 420px
- Maximum height: 85% of viewport
- Fully responsive width

Adjust `aspect-ratio` for different proportions. For mobile-first layouts, try `aspect-ratio:3/4`.

## Squarespace Integration

1. Add a **Code Block** to your page
2. Set it to HTML mode
3. Paste the embed code above
4. Replace `<your-pages-url>` with your GitHub Pages URL

Note: Some Squarespace plans require Business tier or higher for iframe support.

## Security Notes

- GitHub Pages does not send `X-Frame-Options` or `frame-ancestors` headers
- The viewer does not set frame restrictions
- The viewer is designed to be embedded safely

## Browser Compatibility

The viewer requires:
- Modern browser with WebGL support
- JavaScript enabled
- ES6 module support
