---
title: CV — Lê Quang Tuệ
---

# Lê Quang Tuệ

**Geospatial Engineer · Data Journalist** — Ho Chi Minh City, Vietnam (UTC+7)
lequangtuevn@gmail.com · [github.com/lqtue](https://github.com/lqtue) · [linkedin.com/in/lqtue](https://vn.linkedin.com/in/lqtue) · [maparchive.vn](https://maparchive.vn)

Available for remote, deliverable-scoped work.

---

## Summary

I build geospatial data pipelines end to end and ship them to production on my own: national-scale building datasets, OpenStreetMap completeness measurement, and automated georeferencing of historical map series. Python and PostGIS on the data side, TypeScript and OpenLayers on the surface, and a habit of measuring whether a method works before recommending it. Award-winning data journalist before that, which is why every pipeline I build ends in something a non-specialist can read.

---

## Experience

### Founder & Lead Developer — Vietnam Map Archive · 2025 – present
Open research infrastructure for the spatial history of Saigon. Live at [maparchive.vn](https://maparchive.vn); 413 commits, single author.

- Automated georeferencing of the **US Army L7014 series** (535 sheets, 1:50,000 Vietnam): neatline clipping, warping, and a single raster tile archive — including an **Indian 1960 → WGS 84 Helmert correction** with a validation probe, because the standard transformation path silently returns unshifted coordinates over half the study area. Adjacent sheet edges agree to 2.5–14 m.
- **Self-hosted basemap**: a 348 MB Protomaps/OpenStreetMap PMTiles archive for Vietnam plus a shallow regional archive, served with byte-range caching — removing a third-party raster dependency.
- **Production LLM extraction**: schema-constrained Gemini Flash over tiled sheets producing toponyms with oriented bounding boxes and ground coordinates; a published evaluation baseline against a human-validated ground-truth set; per-call cost accounting before scale-up.
- **Segmentation**: fine-tuned SAM2 (LoRA) prompted from text detections, producing building footprint candidates for human validation.
- **Platform**: SvelteKit 5, OpenLayers and Allmaps; Supabase/PostGIS with 78 migrations and state transitions implemented as Postgres functions; a job queue using `FOR UPDATE SKIP LOCKED` with a Python worker; 208 automated tests; IIIF v2/v3 ingestion with Internet Archive redundancy.
- Corpus: 101 maps, 39 georeferenced, 394 grouped historical place names, coverage 1791–1900s across Saigon, Hanoi, Huế and Gia Định.

### Geospatial & AI/LLM Specialist — Vietnam Wartime Accounting Initiative, Texas Tech University · 2026
Remote contract on a US-Congress-established humanitarian program to help account for more than 200,000 missing Vietnamese soldiers and civilians. Georeferencing of wartime maps and sketches; conversion of wartime grid references, UTM zones and the Indian 1960 datum to modern frameworks; AI-assisted extraction of names, dates, units and places from degraded and handwritten archival material; entity linking for case reconstruction. Technical lead of the team's AI/ML proposal covering a 261,000-file, 2.7-million-page collection.

### Map Operations Engineer — VTII / Tasco Maps · 2026
Map-quality and 3D-building data science for a commercial mapping platform.

- **National building data in GeoParquet** for Vietnam: Google Open Buildings (66.1M polygons), Global Building Atlas (57.3M), Meta HRSL (34.1M points), Overture and Microsoft builds.
- **Height benchmark that changed the product plan**: open global products correlate 0.83–0.85 with OpenStreetMap levels in aggregate, but stratified the correlation collapses to r ≈ 0.02 for 1–3 storey buildings — 93% of the fabric — with a near-constant height emitted across the whole low-rise class. Conclusion, reached two independent ways: these products are presence detectors, not geometry sources, in dense Vietnamese urban fabric.
- **Hanoi completeness index**: 3,991 H3 cells × 33 columns; a building deficit of 0.893 against a road deficit of 0.12, which set the collection plan. Independently reproduced the published urban-mapping U-curve on Hanoi through a different data path, locating the worst-mapped fabric in the 15–25 km peri-urban ring.
- **Tasking model**: greedy marginal value per effective cost, recomputed after each pick, with Beta posteriors per cell and an explicit stopping rule. Audited my own model, found and costed 17 defects, and shipped a decision register with 7 retractions and 6 kill conditions.
- **Cadastral fusion**: parcel sources scraped and polygonized into topologically exact coverage; fusion raised ward coverage from 33% to 46% and recovered 213 alleys with no OpenStreetMap way at all.
- **3D vendor specification**: authored the LOD1/2/3 requirements brief for a mobile MapLibre product and pinned the LOD definitions to the published literature, preventing a costly re-bake.

### Data Journalist — VnExpress, Spotlight Desk · 2024 – 2026
Built the data infrastructure behind the coverage, not only the graphics: a typhoon platform crawling NOAA/JTWC into PostGIS behind a REST API; hourly crawlers for 16 river stations and 22 reservoirs; commune-level landslide and flash-flood risk maps; a ward-lookup tool for Vietnam's 2025 administrative merger; a national power-infrastructure dashboard. Credited as *Dữ liệu và Đồ họa: Quang Tuệ*.

Earlier: **Journalist**, VnExpress International, Business Desk (2022); **Journalist**, Zing News, World Desk (2021). **Media & Communications Officer**, Fulbright Urban Social Economics (2024–).

---

## Awards

- **Giải C — National Press Award (Giải Báo chí Quốc gia) XIX**, 2024. Data-driven longform on Typhoon Yagi.
- **Giải B — Hội Báo Toàn Quốc**, 2025. Interactive retrospective on 30 April 1975.

## Publication

Lê, Q. T. (2026). *Urban Green Cover and Land Surface Temperature in Ho Chi Minh City: A Remote Sensing Analysis of Vegetation Cooling Effects Across Historical Development Rings, 1990–2025.* EarthArXiv. [doi:10.31223/X5NJ4B](https://doi.org/10.31223/X5NJ4B). Sole author.

## Skills

**Data** — Python (pandas, geopandas, shapely, rasterio, GDAL/OGR), PostgreSQL/PostGIS, GeoParquet, H3, OpenStreetMap tooling, Bayesian estimation
**Geo** — CRS and datum work (Helmert, Indian 1960, VN2000, UTM), georeferencing and GCP propagation, PMTiles and tile pipelines, IIIF, Allmaps, QGIS, Sentinel-2 / NDVI / LST, CityJSON and 3D Tiles
**Build** — TypeScript, SvelteKit, OpenLayers, MapLibre GL, Supabase, Cloudflare Pages/R2/D1/Workers, Playwright, Postgres job queues
**AI** — schema-constrained LLM extraction pipelines, document and map OCR, SAM2 / LoRA fine-tuning, human-in-the-loop review design

## Education

**Fulbright School of Public Policy and Management** — Master of Public Policy; coursework completed, thesis not submitted.
**University of Social Sciences and Humanities, VNU-HCMC** — BA, International Relations.

## Languages

Vietnamese (native) · English (professional)
