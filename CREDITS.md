# Profile artwork

The animated header is rendered from [Thomas Chuang’s interactive portfolio](https://thomas-chuang.com/#proj-historical-map-geoai). The name remains fixed while modern satellite imagery rewinds to the same location on a 1921 map, which is then outlined, extracted, scanned, classified, and turned into a 3D landscape.

- Satellite imagery: [Esri World Imagery](https://services.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer), © Esri and Vantor. The visible crop contains imagery acquired in 2021–2025, so the animation labels the mosaic “2020s,” rather than claiming one capture year. Imagery and historical maps use matching Web Mercator extents; the release includes source metadata and the crop registration.
- Historical map: 1921 Taiwan map, Academia Sinica [Taiwan Historical Maps](https://gissrv4.sinica.edu.tw/gis/twhgis/), layer `JM20K_1921`.
- Classification: Thomas Chuang’s recorded sliding-window model output. The network activity is illustrative; percentages show each class’s share of the classified pixels in the complete map, excluding unclassified pixels. They are area percentages, not confidence scores.
- Elevation: Ministry of the Interior [20 m digital terrain model](https://data.gov.tw/dataset/176927), displayed with 6× vertical exaggeration.
- Houses and vegetation are cartographic symbols placed within predicted classes, not recovered building footprints or measured counts.
- Technology marks: [Simple Icons](https://simpleicons.org/), distributed through react-icons. Names and logos belong to their respective owners.

Animation files and static posters are hosted as [versioned release assets](https://github.com/chuang091/chuang091/releases/tag/profile-art-v5), outside the Git history. The README selects one image for the viewer’s screen and color scheme, and a static poster when reduced motion is requested.

The complete 24-second loop retains the satellite comparison, map extraction, neural-network illustration, classification, and 3D terrain growth. The name and palette sit above the animation, giving the artwork the full card width. The classification readout has more space between the map, heading, and rows. Desktop delivery is 2400 × 2280; mobile is 1440 × 1629. Full-color animated AVIF is preferred, with an animated WebP fallback at 1600 × 1520 (desktop) or 1152 × 1303 (mobile), and a static poster for reduced motion. Only the selected format, layout, and theme are requested. Exact sizes, encoding settings, and SHA-256 checksums are recorded in the release manifest.

## Map projects

Two clickable animations below the contact links use the same recorded geography as the interactive portfolio.

- **Convenience-store analysis:** 1,534 recorded store positions from the [original feature service](https://services6.arcgis.com/gDvgvk6tNkAnOdO4/arcgis/rest/services/%E8%B6%85%E5%95%861082nd/FeatureServer/0), registered to the Taipei analysis bounds in EPSG:3826. The city unfolds into road connections, population, bus stops, MRT stations, and YouBike stations; the original vectors become display-normalized factor grids and combine into the [recorded suitability result](https://github.com/chuang091/MGWR/tree/main/Results/Suitability). These are research data, not a live inventory or proposed store locations.
- **City outline:** the alpha contour of the [Taipei City Government zoning dataset](https://data.taipei/dataset/detail?id=3bab0a01-7936-4218-8cb5-f74dfcb43dda), used as a neutral silhouette behind the stores.
- **YouBike:** 658 paths derived from the [original vector-field raster](https://tiledimageservices6.arcgis.com/gDvgvk6tNkAnOdO4/arcgis/rest/services/c10000/ImageServer). Moving trails illustrate that field, rather than individual recorded trips or measured cycling speed. The full research project is [YouBikeAnalysis](https://github.com/chuang091/YouBikeAnalysis).
- **Contemporary street context:** © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), ODbL. Analysis colors, vertical layer separation, and camera movement are display choices.

The map cards use 2400 × 1800 desktop images and 1440 × 2475 portrait images, with separate light and dark palettes. Animated AVIF is preferred; WebP and static reduced-motion posters are included. Factor grids, the assembled layers, and the final result hold before the next transformation. The header's neural illustration and classification have longer reading time without increasing its encoded image size. Source hashes and frame durations are included in the release manifest and map-source metadata.
