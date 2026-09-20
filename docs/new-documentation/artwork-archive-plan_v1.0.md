# Artwork Archive Plan v1.0

*Where every work of art lives, at what resolution, under what license. Drafted 2026-09-20.*

---

## 1. The pipeline (one job per platform)

| Platform | Role | What lives there |
|---|---|---|
| GitHub (`works` repo) | **Catalog** | Metadata, web-resolution images, cross-references, version history |
| Internet Archive | **Vault** | Full-resolution masters, permanent URLs, free and unlimited |
| Zenodo | **Citation** | DOI-versioned releases (series catalogs, official documents) |

Rule: work in GitHub, preserve on IA, cite via Zenodo. The GitHub record always links to
the IA item; the IA item always links back to the GitHub record.

## 2. Internet Archive structure

- **One top-level collection:** `the-historiotheque` — the whole oeuvre.
- **Sub-collections** per series: `chronotopium-series`, `noise-fields`, `anatomy-of-an-aesthetic-problem`, …
- **One item per work.** Item identifier pattern:
  `historiotheque-<series>-<work-slug>-<year>`
  e.g. `historiotheque-chronotopium-no11-2026`.
- **Each item holds:** the master image file(s) + a `metadata.txt`/`README.md` with the
  fields below. IA generates its own metadata record from these.
- **Per-item metadata:** title · creator (A.G. / Alex Gagnon) · date · series ·
  medium · dimensions (physical, for analog) · pixel dimensions (for digital) ·
  description · license · `github:` link to the `works` repo entry ·
  `refcards:` IDs where relevant.

## 3. GitHub `works` repo structure

```
works/
├── README.md                    # the catalog: what it is, how to read it, license
├── chronotopium-series/
│   ├── index.md                 # series overview + work list
│   └── no-11/
│       ├── work.md              # full metadata (frontmatter below)
│       └── no-11_web.jpg        # web-resolution display copy
├── noise-fields/
│   └── …
└── …
```

`work.md` frontmatter:

```yaml
---
title: "Chronotopium No. 11"
series: chronotopium-series
date: 2026-09-18
medium: "mixed media on cardboard"     # or "digital painting"
dimensions_physical: "60 x 45 cm"      # analog only
dimensions_px: "6000x4500"             # master resolution
master_location: "https://archive.org/details/historiotheque-chronotopium-no11-2026"
license: CC-BY-NC-4.0
refcards: []
related_logs: []
---
```

## 4. Capture standard (going forward)

### Analog paintings (photographing the work)
- **Minimum:** 4000 px on the longest edge; 300 DPI at intended reproduction size.
- Shoot **RAW + JPEG**; the RAW (or highest-quality TIFF export) is the master.
- Tripod, diffuse natural light, no on-camera flash; square the camera to the work.
- Include a neutral color reference in one frame if available (even a printed gray card).
- File naming: `<series>-<work>-<year>-master.<ext>` (e.g. `chronotopium-no11-2026-master.tif`).

### Digital paintings
- Export masters at **print resolution**: minimum 6000 px longest edge, PNG or TIFF.
- Keep the **working file** (layered source) alongside the flattened master.
- Social/web exports are *display copies*, made from the master — never the other way around.

### Display copies & AI upscaling
- Display copies (GitHub, social): web resolution, exported from the master.
- AI upscaling is permitted **only for display copies**, and any upscaled file must be
  labeled as such in its metadata (`processing: ai-upscaled`). The master is always the
  true original. (Per the New Documentation: the archive does not silently fabricate.)

## 5. Backfill (existing works)

1. **Inventory first:** list every work with honest resolution metadata — no shame in
   "1200 px, phone photo, 2019." The honest record is the point.
2. Originals become masters as-is; note `master_quality: legacy` in the metadata.
3. Where a better capture is possible (the painting still exists), re-photograph to the
   capture standard and supersede the old master — keep both, link both, date both.
4. Upload in series batches to IA; register each in the `works` repo as you go.

## 6. Licensing (decision needed)

The documents carry "© A.G. All Rights Reserved." For the artwork archive, "free and
accessible to the public" suggests a Creative Commons license. Candidates:

- **CC BY-NC 4.0** — free to share and adapt, non-commercial, attribution required.
  Protects against commercial exploitation while keeping everything open.
- **CC BY 4.0** — same, but commercial use allowed.
- **CC0** — public domain dedication; maximum openness, no control retained.

Recommendation: CC BY-NC 4.0 as the default — open to the public, closed to exploiters.
One license for the whole archive keeps it clean; exceptions noted per work.

**Does CC BY-NC stop the artist making money? No.** A CC license is non-exclusive: the
artist keeps full copyright and can still sell originals, sell prints, and grant separate
commercial licenses (dual-licensing is standard). The NC clause restricts *other people's*
commercial use, not the artist's own. "All Rights Reserved" also remains fully available
on GitHub and the Internet Archive — neither platform forces a CC license — but it also
blocks non-commercial sharing, which works against the discoverability the archive is for.

## 7. Seeding order

1. Create the IA `the-historiotheque` collection.
2. Create the `works` repo with the structure above and one fully-worked example entry.
3. Set the license (see §6).
4. Backfill series by series, newest first (best masters first, momentum matters).
5. When a series is complete on IA, cut a Zenodo DOI release for its catalog.
