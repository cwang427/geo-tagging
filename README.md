# Landscape Zone Planner

A single-page web app for drawing irrigation zones as editable, colour-coded shapes on satellite imagery. It is built as the first layer of a multi-layer landscape plan.

Everything is in `index.html`. There is no build step and no server.

## Features

- **Zone shapes**: trace any polygon, or a quick rectangle. Drag corners to reshape, drag the midpoint dots to add corners, or drag the whole zone.
- **Cut hole**: cut patios, tree rings or other areas out of a zone.
- **Colour coding**: each zone gets its own colour. Pick from the palette or any custom colour.
- **Zone details**: number, name, notes and live area (ft² / acres), plus total irrigated area.
- **Points**: valves, controller, backflow, water source, hose bibs, sensors and heads. A point can be linked to the zone it serves.
- **Layers panel**: show/hide, fill opacity and label toggle. The `LAYER_TYPES` registry in `index.html` is where planting, hardscape, lighting and other layers get added later.
- **Map**: Esri satellite imagery (zoom to about 22), street map toggle, road labels overlay, address search, and "locate me" GPS.
- **Saving**: autosaves in your browser. **Export GeoJSON** to back up or move to another device, and **Import** to restore or merge. GeoJSON also opens in QGIS, geojson.io and other GIS tools.
- Works on desktop and phone. On narrow screens the panel becomes a collapsible bottom sheet.

### Keyboard

- `Esc` cancels a drawing tool or deselects.
- `Delete` / `Backspace` deletes the selected zone or point.

## Deploy to GitHub Pages

1. Merge this branch into `main`, or deploy from the branch directly.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, pick the branch and `/ (root)`, then **Save**.
4. After a minute or so, the site is live at `https://<your-username>.github.io/geo-tagging/`.

## Your data

Data is stored in your browser's local storage for that site, so it does not sync between devices or browsers. Clearing site data erases it. Export regularly, and keep the `.geojson` file somewhere safe. Committing it to this repo works too.

## Credits

[Leaflet](https://leafletjs.com) · [Leaflet-Geoman](https://geoman.io) · imagery © Esri, Maxar, Earthstar Geographics · street map © OpenStreetMap contributors · search by Nominatim.
