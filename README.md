# Hive Thermal / Humidity / Colony Visualizer

An interactive 3D viewer for exploring thermal, humidity, and colony dynamics in a 10-frame Langstroth beehive simulation.

## Features

- **3D visualization** with temperature and relative humidity fields interpolated between model nodes
- **Condensation display** showing films on inner surfaces and under covers
- **Energy flow arrows** indicating heat transfer
- **Synchronized time-series charts** for temperature, humidity, honey stores, and heat budget
- **Interactive controls** including cross-section planes, transparency settings, and time scrubber
- **Embed mode** for integration into other websites

## Viewing the Simulation

Open `index.html` through any static web server. GitHub Pages works out of the box. Local `file://` URLs do not work due to ES module and fetch requirements.

**URL Parameters:**
- `?embed=1` — hides side panels; use ☰ button to show controls
- `?run=<id>` — selects a specific scenario
- `?k=<step>` — sets the starting time step
- `?geom=parametric` — uses parametric geometry (default)

**Controls:**
- ⛶ toggles full screen mode
- Responsive layout: stacks vertically on narrow screens

## About the Model

The simulation uses a lumped-node thermal and humidity model with stratified air layers and cluster core/mantle dynamics. **The model is uncalibrated and intended for comparing different hive configurations, not for absolute measurements.** Treat numerical values as order-of-magnitude estimates.

**Included scenarios:**
- Edmonton baseline: one-year simulation of a wooden hive (3-hour intervals)
- Winter day: 24-hour January simulation in Edmonton (10-minute intervals)

## Deploying to GitHub Pages

1. Create a GitHub repository
2. Push this folder to the `main` branch
3. In repository **Settings → Pages**, set **Source** to "Deploy from a branch"
4. Select **main** branch and **/ (root)** folder
5. Save and wait for deployment

The site will be available at `https://<username>.github.io/<repository>/`

The `.nojekyll` file ensures GitHub Pages serves the files without Jekyll processing.

## License

© 2026 ALTAY Custom Plastics. All rights reserved.

The visualization uses Three.js (MIT license, see `vendor/THREE_LICENSE`).
