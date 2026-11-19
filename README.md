# Europa Clipper Ephemeris Observatory

A static observing dashboard built from a JPL Horizons ephemeris for Europa Clipper, observed from KFUPM in Dhahran, Saudi Arabia.

## Publish with GitHub Pages

1. Create a GitHub repository for the site.
2. Upload all files in this folder to the repository root. Keep `index.html` and `ephemeris.json` together; the dashboard loads the data file by relative path.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. After GitHub Pages finishes deploying, use the URL shown in the Pages settings.

GitHub Pages publishes a publicly accessible website. This is a static copy and is separate from the private ChatGPT Site.

## Dashboard contents

- JPL Horizons ephemeris table and observer plots
- Local Dhahran time (AST, UTC+3) and UT display
- Calculated altitude and azimuth for KFUPM/Dhahran (26.307° N, 50.146° E)
- Interactive north-facing panorama with a timeline slider and play/pause control

## North-facing simulation limits

The panorama is an idealized 180° forward view: west (azimuth 270°) on the left, north (0°) in the center, and east (90°) on the right. It plots the spacecraft's apparent direction from the selected ephemeris sample. It is not a camera image: visual magnitude was not included, and the simulation does not model apparent brightness, angular size, background stars, terrain, atmospheric refraction, or local obstructions.

Altitude and azimuth are calculated from the apparent RA/Dec and the observer location using sidereal time. They are geometric values; atmospheric refraction is not applied. The JPL ephemeris has daylight skipping enabled, and the spacecraft trajectory is a prediction. Refresh the ephemeris from JPL Horizons before planning an observation.

## Files

- `index.html` — dashboard and interactive simulation
- `ephemeris.json` — source ephemeris samples
- `.nojekyll` — serve the static files without a Jekyll build
