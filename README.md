# GlobeAll camera catalogue

Generated data only. No source code lives here — see the note at the bottom.

- **Built** 2026-09-07T06:17:37Z
- **Cameras** 8,660 from 5 public agencies
- **With a written description** 2,220 (26%)
- **Not yet scorable** 1,062 — no cached gazetteer for Canada

## Files

| file | what it is |
|---|---|
| `catalogue.json` | every camera, its rights record, and its computed description |
| `ATTRIBUTION.md` | the source, licence basis and credit line for every row |
| `index.json` | this summary, machine-readable |

## What a description looks like

- **US-101 : S of SR 271 - Looking South (C030)** — Bear Pen Creek, on the right — two rivers in view.
- **US-101 : South Of SR-36 - Looking North (C013)** — Barber Creek, on the left, a way off, Rohnerville Airport beyond.
- **US-101 : South Of SR-36 - Looking South (C013)** — Barber Creek, on the left, a way off, Rohnerville Airport beyond.
- **US-101 : Eureka / 5th & R Street - Looking North (C034)** — Daby Island, dead ahead — two islands in view.

Descriptions are computed from camera position and bearing against a public gazetteer,
then written from those computed facts. Nothing is derived from the camera image.

A camera is described only if it scores at or above **0.64** on a peer-normalised
interestingness score. Below that it gets its label and nothing else — most public cameras
point at unremarkable road, and a paragraph about each would be worth less than silence.

## Rights

Every row carries the licence it is published under, the terms URL, and the exact credit
string its operator asks for. See `ATTRIBUTION.md`.

## Why this repository is public

GitHub Pages serves it for free without a payment card. It receives one generated file
and never any source: the application and the pipeline that builds this are private.
