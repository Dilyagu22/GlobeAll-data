# Terrain: the coarse whole-Earth tier

Source: **Copernicus DEM GLO-90** (Copernicus WorldDEM™-90, 3 arc-second global Digital Surface
Model, `COP-DEM_GLO-90-DGED` reprocessed to Cloud Optimized GeoTIFF), read keylessly from the AWS
Open Data bucket `s3://copernicus-dem-90m` (`arn:aws:s3:::copernicus-dem-90m`, eu-central-1; the
AWS Open Data registry publishes `aws s3 ls --no-sign-request s3://copernicus-dem-90m/` as the
account-free route, and these cells were fetched by anonymous HTTPS GET from
`https://copernicus-dem-90m.s3.amazonaws.com/<name>/<name>.tif`), masked to land by that bucket's own `tileList.txt`
(26,475 one-degree geocells, fetched 2026-09-09) and baked to LERC tiles at levels
0–7 with a maximum error of 5 m (12,648 tiles, 12,652 files,
253,833,493 bytes = 242.1 MiB). Copernicus publishes no ocean tiles — absent ocean reads as zero — and ground
below sea level is kept, not clamped. Baked 2026-09-09.

Licence: **Licence for COP-DEM-GLO-90-F Global 90m Full, Free & Open — Licence for the use of the
Copernicus WorldDEM™-90**, Article 4 granting reproduction, distribution, communication to the
General Public, and adaptation. Fetched 2026-09-09 from
`https://dataspace.copernicus.eu/sites/default/files/media/files/2025-06/copernicus_contributing_mission_data_access_v2_cop_dem_licenses.pdf`
(HTTP 200, 499,914 bytes, sha256 `bb4a01dcd7f61acefa81c9ccd76af975e12096158169acf0d7b5c44c26c8701f`,
pages 19–21), and identically from the ESA Mission-specific Annex at
`https://s3.waw3-1.cloudferro.com/swift/v1/portal_uploads_prod/CSCDA_ESA_Mission-specific_Annex_31_Oct_22_latest.pdf`
(HTTP 200, 532,208 bytes, sha256 `d8284dfa026f192c1d4f212b2846168720363dbe0ee112bfbceeb66d870a77b7`,
pages 18–20). Article 5: *"The use rights granted under this licence are free of charge to the
User."* Article 3: *"The rights granted under this Licence are worldwide and without limitation in
time."*

These tiles are adapted from the source, so the licence's Article 6(b) notice is the one that
applies, quoted character for character from the instrument (its own opening `"` and closing `”`
are reproduced as printed):

> (b) Where the Copernicus WorldDEM™-90 data have been adapted or modified, the User shall provide the following notice:
> "produced using Copernicus WorldDEM™-90 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved”.

**The credit line these tiles carry, and that the app must display:**

> produced using Copernicus WorldDEM™-90 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved

Article 6(c) requires a liability sentence in any notice covering distribution or communication to
the General Public. It is carried here verbatim:

> "The organisations in charge of the Copernicus programme by law or by delegation do not incur any liability for any use of the Copernicus WorldDEM™-90".

Nothing here is officially endorsed by Airbus Defence and Space GmbH, DLR, ESA, the European Union
or any other body in charge of the Copernicus programme (Article 6(d)). Anyone redistributing these
tiles, modified or not, is bound by the same obligations (Article 6(e)).

Citation DOI for the dataset, as the Copernicus Data Space Ecosystem asks: `https://doi.org/10.5270/ESA-c5d3d65`.

**No restriction bars this use.** The GLO-90-F licence contains no non-commercial clause, no
no-redistribution clause and no share-alike. Measured across its whole text — pages 19–21 of the
CDSE licence PDF and pages 18–20 of the ESA Mission-specific Annex — the strings `commercial`,
`redistribut`, `shall not`, `may not`, `must not`, `share-alike`, `same terms`, `same licence`,
`prohibit`, `resell`, `royalty`, `internal use` and `personal use` each occur **zero** times.
`charge` occurs six times in each instrument and never as a restriction: the Preamble's
"free-of- charge basis", Article 5's "free of charge to the User", and four times as "in charge
of the Copernicus programme". (The non-commercial terms elsewhere in the same PDF belong to
the Copernicus Contributing Mission licence at pages 1–10, whose clauses sit on pages 5 and 6, and
to the restricted COP-DEM-GLO-30-R / COP-DEM-EEA-10-R licence at pages 11–18, whose clause sits on
page 15. Neither governs GLO-90, which is pages 19–21.)

Served as an ArcGIS tiled elevation service description (`index.json`) plus
`tile/{level}/{row}/{col}` LERC1 tiles, by the GlobeAll project (free, non-commercial).
