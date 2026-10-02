# Profile artwork

The animated header is rendered from [Thomas Chuang’s interactive portfolio](https://thomas-chuang.com/#proj-historical-map-geoai). The name remains fixed while modern satellite imagery rewinds to the same location on a 1921 map, which is then outlined, extracted, scanned, classified, and turned into a 3D landscape.

- Satellite imagery: [Esri World Imagery](https://services.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer), © Esri and Vantor. The visible crop contains imagery acquired in 2021–2025, so the animation labels the mosaic “2020s,” rather than claiming one capture year. Imagery and historical maps use matching Web Mercator extents; the release includes source metadata and the crop registration.
- Historical map: 1921 Taiwan map, Academia Sinica [Taiwan Historical Maps](https://gissrv4.sinica.edu.tw/gis/twhgis/), layer `JM20K_1921`.
- Classification: Thomas Chuang’s recorded sliding-window model output. The network activity is illustrative; percentages show each class’s share of the classified pixels in the complete map, excluding unclassified pixels. They are area percentages, not confidence scores.
- Elevation: Ministry of the Interior [20 m digital terrain model](https://data.gov.tw/dataset/176927), displayed with 6× vertical exaggeration.
- Houses and vegetation are cartographic symbols placed within predicted classes, not recovered building footprints or measured counts.
- Technology marks: [Simple Icons](https://simpleicons.org/), distributed through react-icons. Names and logos belong to their respective owners.

Animation files and static posters are hosted as [versioned release assets](https://github.com/chuang091/chuang091/releases/tag/profile-art-v3), outside the Git history. The README selects one image for the viewer’s screen and color scheme, and a static poster when reduced motion is requested.

The complete 21-second loop retains the satellite comparison, map extraction, neural-network illustration, classification, and 3D terrain growth. The classification readout uses larger type and spacing. Desktop delivery remains 2400 × 1040; mobile is 1440 × 1314. Full-color animated AVIF is preferred, with an animated WebP fallback at 1920 × 832 (desktop) or 1152 × 1051 (mobile), and a static poster for reduced motion. Only the selected format, layout, and theme are requested. Exact sizes, encoding settings, and SHA-256 checksums are recorded in the release manifest.
