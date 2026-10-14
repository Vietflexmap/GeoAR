# Vietflexmap GeoAR Atlas

WebGIS + FieldGIS + experimental outdoor camera AR. Demo data is fictional.

## Quick start
Open `index.html` through an HTTPS static host (GitHub Pages), or serve locally at localhost.

**Repository:** https://github.com/Vietflexmap/GeoAR  
**Suggested Pages URL after deployment:** https://vietflexmap.github.io/GeoAR/

## Features
- MapLibre GL JS raster OpenStreetMap basemap with visible OpenStreetMap attribution.
- GIS point assets: survey markers, electric poles, water valves, manholes, other.
- Add/edit/delete/search/filter point assets with coordinate validation.
- Import GeoJSON FeatureCollection (Point geometries), upsert by ID; export GeoJSON.
- Model preview via `model-viewer`: public HTTPS GLB/GLTF or temporary local upload.
- Field report as CSV and downloadable printable HTML.
- Experimental camera view with GPS/compass-derived 2D labels for nearby assets.

## Safety, limits, and accuracy
- **AR is approximate**: camera overlays are not physically anchored 3D; unsuitable for excavation, surveying, locating actual buried utility lines or safety critical decisions.
- GPS / compass accuracy depends heavily on phone hardware, calibration, weather and surroundings.
- Stored data stays only in browser localStorage; no account sync, team edits or authentication.
- Local GLB uploads are temporary blob URLs; model files are not saved in GeoJSON. Publish 3D files on a suitable HTTPS server and use their URLs for sharing.
- Third-party libraries and map tiles require internet. For production, self-host dependencies and use a tile provider suitable for your traffic volume. Do not bulk download tiles from tile.openstreetmap.org.
- Demo coordinates and asset information are intentionally fabricated.
- Import limit 10 MB GeoJSON; local GLB limit 25 MB.
- For cross-platform browser support, verify camera, GPS and orientation permissions on physical mobile devices.

## Deploy to GitHub Pages
In GitHub repository Settings → Pages → Build and deployment → Deploy from a branch → main → /(root). Use the generated HTTPS URL; mobile camera needs secure context.

## Roadmap
1. IndexedDB and local persistent GLB attachments.
2. Multi-user authentication, PostGIS, access control and synchronization.
3. Real geospatial AR anchors with field calibration and RTK GNSS support.
4. Offline tiles and audited field QA/QC workflow.
5. Customer workspaces, subscription billing and managed hosting.

## Open-source components
- MapLibre GL JS (BSD-3-Clause)
- OpenStreetMap data / tile rendering (observe ODbL attribution and tile use policies)
- Google model-viewer (Apache-2.0)

Verify transitive dependencies and licenses before redistributing as a commercial product.

© 2026 Vietflexmap. Repository license remains unspecified until the maintainer chooses a license.
