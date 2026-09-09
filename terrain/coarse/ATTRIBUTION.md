# Terrain: the coarse whole-Earth tier

Source: NOAA NCEI **ETOPO 2022** (15 arc-second ice-surface global relief model, 288 GeoTIFF tiles), baked to
LERC tiles at levels 0–7 with a maximum error of 5 m; ocean and below-sea-level ground set to zero.

Licence, quoted from NOAA's ISO metadata for ETOPO 2022 (fetched 2026-09-09):
> These data were produced by NOAA and are not subject to copyright protection in the United States. NOAA waives any potential copyright and related rights in these data worldwide through the Creative Commons Zero 1.0 Universal Public Domain Dedication (CC0-1.0).

Served as an ArcGIS tiled elevation service description (`index.json`) plus `tile/{level}/{row}/{col}` LERC1 tiles, by the GlobeAll project (free, non-commercial).
