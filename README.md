# PS1 Discovery Corpus

A multilingual metadata corpus of **7,995 PlayStation 1 games**, built to be searched
**by feel** — *"a 1996/97 Japanese game where you could send letters"*, *"a cozy
fishing game with an anime aesthetic"*, *"a bleak sci-fi adventure nobody remembers"* —
rather than by popularity or rigid filters. It is deliberately biased toward **obscure
and Japan-exclusive titles**: the long tail most databases skip.

The dataset's value is its **editorial layer**: every row carries an original,
evidence-grounded short description and a set of controlled-vocabulary tags spanning
mood, setting, mechanics, cultural lineage, and quality — the axes you actually search
by when you half-remember a game.

## What's in the box

| File | What it is |
|------|------------|
| `ps1_corpus.csv` | The corpus — 7,995 rows × 127 columns (UTF-8, ~31 MB). |
| `ps1_corpus.parquet` | Same data, Apache Parquet (typed, ~6 MB) — recommended for analysis. |
| `tag_vocabulary.json` | The 330-tag / 10-dimension controlled vocabulary (machine-readable). |
| `DATA_DICTIONARY.md` | Every column: type, coverage, source, licensing, description. |
| `TAG_VOCABULARY.md` | Human-readable tour of the tag dimensions. |
| `ATTRIBUTION.md` | Per-source attribution + licensing (the share-alike backbone). |
| `LICENSE` / `NOTICE` | CC BY-SA 4.0 + the per-component attribution/terms. |

## At a glance

- **7,995 games** — 7,861 with a full PlayStation DataCenter catalogue entry, plus 134
  thin wiki-only stubs (flagged `is_stub=1`) for real games with no catalogue page.
- **Release years 1994–2007**; regions NTSC-J / NTSC-U / PAL (Japan-heavy by design —
  ~4,400 rows are Japan-only).
- **Editorial layer (this project's own work):** a `curated_short_desc` on 100% of rows
  and **16.7 tags/game** on average from a 330-tag vocabulary.
- **Multilingual:** Wikipedia lead-summary extracts in **10 languages** (EN, JA, FR, DE,
  IT, ES, KO, RU, PT, PL) on 3,384 rows, plus native-script titles. (A Chinese-localization
  tracker is also present but only on 6 rows — see the data dictionary.)
- **30+ upstream sources** reconciled into one row per game (see ATTRIBUTION.md).

## How to use it for "find by feel"

The `curated_short_desc` and `tags` columns are designed as the search surface. A typical
pipeline: embed `curated_short_desc` (optionally concatenated with the flattened `tags`)
with a sentence-transformer, then rank by cosine similarity to a natural-language query.
The `tags` JSON also supports structured filtering (e.g. `setting` contains `Cyberpunk`
**and** `mood` contains `Melancholic`).

```
tags example (JSON object, one list per dimension):
{"genre": ["Survival-Horror"], "mood": ["Tense"], "setting": ["Mansion"],
 "mechanic": ["Polygonal-3D","Save-Point"], "cultural_lineage": ["Japanese-Design"],
 "discovery": ["Cult-Classic"], "quality": ["Quality-Strong"], ...}
```

**Types differ by format.** In **Parquet**, `is_stub` is a native boolean and numeric columns
are typed (int/double) — recommended for analysis. In **CSV**, everything is text: `tags` is a
JSON-encoded string (`json.loads` it), `is_stub` is the literal `True`/`False`, and numbers are
strings. Every row has all 10 tag dimensions present; an abstained dimension is an explicit
empty list (`[]`), so structured filters never hit a missing key.

## Coverage caveats (read before drawing conclusions)

- **Editorial descriptions are universal; structured enrichment is not.** Facts and our
  own tags/descriptions cover every row, but third-party facets are filled only where a
  source had data. Evidence-gated tag dimensions (mood, setting, quality) are intentionally
  **left empty when no source supports them** rather than guessed — abstention is a feature.
- **The 134 stubs** (`is_stub=1`) are intentionally thin (a real title we couldn't match to
  a catalogue page). Filter them out for a "every row is rich" subset.
- **Japan bias is deliberate**, not a sampling error — it's the point of the project.
- **Third-party editorial prose is not included.** Long-form reviews/articles from sources
  like Hardcore Gaming 101, GameFAQs-style writeups, TVTropes, etc. are **not redistributed**;
  each is kept as a `*_url` pointer so you can follow the link. Our own `curated_short_desc`
  replaces them as the searchable text.

## How it was built (high level)

Each source was ingested into its own table, cross-linked to a PlayStation serial (or a
language-agnostic Wikidata Q-ID), then merged non-destructively into one flat row per game
(sources never overwrite each other; disagreements are kept side-by-side). On top of that
factual base, an editorial pass wrote the tags and short descriptions **from each game's own
evidence** (never from model memory), with an adversarial verification step removing
unsupported claims. Full method and architecture are summarized in ATTRIBUTION.md.

## Licensing

Released under **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** —
see `LICENSE`. In short: use it freely, including commercially; **credit the project and the
upstream sources** (see `ATTRIBUTION.md`); and share derivatives under the same license.

What this is safe to publish under one license: the dataset contains (1) **facts** (titles,
serials, dates, developers, specs, numeric ratings/prices/playtimes, genre labels — not
copyrightable), (2) **our own editorial** (`curated_short_desc`, `tags`), (3) **Wikipedia
lead extracts** (CC BY-SA, attributed), and (4) **Wikidata** identifiers (CC0). Copyrighted
third-party prose and non-commercial (TVTropes) text are **not** included — only links to them.

## Disclaimer

Community research dataset. Not affiliated with or endorsed by Sony Interactive Entertainment
or any listed source. Facts are corroborated across multiple databases but may contain errors;
corrections welcome.
