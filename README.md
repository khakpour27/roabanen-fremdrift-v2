# Røabanen Fremdrift

Gantt-chart visualization for **Rådgiveroppdrag prosjektering — Oppgradering av Røabanen** (Oslo tram line upgrade).

**Live:** <https://khakpour27.github.io/roabanen-fremdrift/>

## Overview

A standalone HTML page showing the 2028 construction schedule across 9 track sections (strekninger), covering preparatory work (March–June) and the main track closure period (3 July – 13 August 2028).

### Features

- **9 section rows** — 8 individual sections + 1 full-line section (Borgen–Eiksmarka)
- **10 time columns** — March (no title), Apr, May, Jun + 6 weekly track-closure columns
- **7 colour-coded work types** — Sporarbeid, Sporveksler, Elektro/kabel, Bru-rehabilitering, Konstruksjon/drenering, Tunnel, Gjerde/sikring
- **Connected spanning bars** — activities running across multiple weeks shown as linked bars with a full-colour connection strip and dimmed continuation boxes
- **3 interactive filters** — Strekning, Arbeidstype, Periode + reset button
- **URL parameter filtering** — `?section=N`, `?type=X`, `?period=X` for embedding
- **Embed mode** — hides header/footer/filters when URL params are present
- **Responsive** — breakpoints at 800 px and 550 px
- **COWI branding** — official SVG logo (linked to cowi.com), corporate colour palette, sticky footer with tagline

## Embed URLs

| # | Section | URL |
|---|---------|-----|
| 0 | Borgen – Smestad | `?section=0` |
| 1 | Smestad – Sørbyhaugen | `?section=1` |
| 2 | Smestad – Makrellbekken | `?section=2` |
| 3 | Makrellbekken – Holmen | `?section=3` |
| 4 | Holmen – Hovseter | `?section=4` |
| 5 | Hovseter – Røa | `?section=5` |
| 6 | Røa – Ekraveien | `?section=6` |
| 7 | Ekraveien – Eiksmarka | `?section=7` |
| 8 | Borgen – Eiksmarka (hele) | `?section=8` |

### Iframe embed example (Esri StoryMap)

```html
<iframe src="https://khakpour27.github.io/roabanen-fremdrift/?section=0"
        width="100%" height="220" frameborder="0"
        style="border:none;overflow:hidden;" scrolling="no"></iframe>
```

## Data source

`Aktivitert i og utenfor brudd.xlsx` — activity schedule with WBS, km ranges, priorities, strekninger, task names, start dates, durations, and finish dates.

## Colour palette (COWI brand)

| Colour | Hex | Usage |
|--------|-----|-------|
| COWI Orange | `#F04E23` | Logo, STENGT SPOR tag |
| Ocean Blue | `#1C2B54` | Header bar, Sporarbeid |
| Aubergine | `#612141` | Sporveksler, STENGT SPOR header |
| Grass Green | `#31B18F` | Elektro / kabel |
| Brick | `#B85042` | Bru-rehabilitering |
| Sand | `#EFE1D6` | Konstruksjon / drenering |
| Steel Blue | `#3B6E9F` | Tunnel |
| Mint Green | `#D5F0E9` | Gjerde / sikring |
| Sky Blue | `#D2EAF7` | Page background |

## Tech stack

Single `index.html` file — no build step, no external dependencies. Pure HTML + CSS + vanilla JavaScript. Hosted on GitHub Pages.

## Local preview

```bash
python -m http.server 3000
```

Then open <http://localhost:3000>.

---

COWI — Together, we shape a sustainable and liveable world
