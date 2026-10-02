# Profile artwork

The animated header is rendered from [Thomas Chuang’s interactive portfolio](https://thomas-chuang.com/#proj-historical-map-geoai). The name remains fixed while the historical map is outlined, extracted, scanned, classified, and turned into a 3D landscape.

- Historical map: 1921 Taiwan map, Academia Sinica [Taiwan Historical Maps](https://gissrv4.sinica.edu.tw/gis/twhgis/), layer `JM20K_1921`.
- Classification: Thomas Chuang’s recorded sliding-window model output. The network activity is illustrative; class percentages come from the recorded classification.
- Elevation: Ministry of the Interior [20 m digital terrain model](https://data.gov.tw/dataset/176927), displayed with 6× vertical exaggeration.
- Houses and vegetation are cartographic symbols placed within predicted classes, not recovered building footprints or measured counts.
- Technology marks: [Simple Icons](https://simpleicons.org/), distributed through react-icons. Names and logos belong to their respective owners.

Animation files and static posters are hosted as [versioned release assets](https://github.com/chuang091/chuang091/releases/tag/profile-art-v2), outside the Git history. The README selects one image for the viewer’s screen and color scheme, and a static poster when reduced motion is requested.

The complete 17.9-second loop uses full-color animated AVIF: 2400 × 1040 on desktop (about 6.3 MB) and 1440 × 1314 on mobile (about 5.5 MB). Animated WebP fallbacks retain the same dimensions at a lower frame rate (about 13.6 MB / 12.4 MB). Only the selected format, layout, and theme are requested.
