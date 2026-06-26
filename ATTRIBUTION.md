# Attribution & Sources

The PS1 Discovery Corpus reconciles **30+ upstream sources** into one row per game. This
file is the attribution backbone required by the dataset's CC BY-SA 4.0 license. The guiding
principle of the release:

- **Facts** (titles, serials, dates, developers/publishers, specs, numeric ratings, prices,
  playtimes, genre/theme **labels**, counts) are not copyrightable. They are corroborated
  across many of the databases below and are included directly.
- **Our own editorial** (`curated_short_desc`, `tags`, `is_stub`) is original work by this
  project, licensed CC BY-SA 4.0.
- **Wikipedia** lead-summary extracts and infobox facts are included under **CC BY-SA 4.0**,
  attributed to Wikipedia and its contributors.
- **Wikidata** identifiers are **CC0** (public domain).
- **Third-party editorial prose** (long-form articles, reviews, narrative writeups) is
  **NOT redistributed** — only the `*_url` pointer to it is kept. **TVTropes** text is
  excluded entirely (CC BY-NC-SA, non-commercial); only its URL and a trope count remain.

## What was taken from each source

| Source | URL | What we included | Notes / license |
|--------|-----|------------------|-----------------|
| PlayStation DataCenter | psxdatacenter.com | Facts: titles, serials, region, dev/publisher, disc specs, dates; **link** | The catalogue spine. Editorial blurbs **not** redistributed (link kept). |
| Wikipedia (EN, JA, FR, DE, IT, ES, KO, RU, PT, PL) | *.wikipedia.org | **Lead-summary extracts, titles, categories, infobox facts** | **CC BY-SA 4.0** — © Wikipedia contributors. |
| Wikidata | wikidata.org | Q-IDs + cross-identifiers | **CC0** (public domain). |
| MobyGames | mobygames.com | Score, genre labels; link | Facts + link only. |
| Redump | redump.org | Per-disc verification facts | Facts only. |
| GameDB-PSX | — | Genre arrays | Facts only. |
| Libretro | libretro.com | Popularity (user count) | Fact only. |
| PSX PAL Database | — | PAL alt-titles, barcodes | Facts only. |
| LaunchBox | gamesdb.launchbox-app.com | Community rating + count, video URL | Facts + link. **Overview prose not included.** |
| IGDB | igdb.com | Themes, perspectives, modes, keywords, ratings, similar-games (names/slugs); link | Facts/labels + link. **Note:** IGDB data is delivered under the IGDB/Twitch API terms; these facets are reproduced as factual labels, not as a redistribution of IGDB's database — verify before high-volume commercial reuse. |
| HowLongToBeat | howlongtobeat.com | Main / extra / completionist hours; link | Facts + link. |
| Hardcore Gaming 101 | hardcoregaming101.net | **Link only** | Long-form articles **not** redistributed. |
| GiantBomb | giantbomb.com | **Link only** | Editorial **not** included (also offline upstream). |
| Speedrun.com | speedrun.com | Category / run counts; link | Facts + link. |
| RetroAchievements | retroachievements.org | Achievement / player counts; link | Facts + link. |
| Hidden Palace | hiddenpalace.org | Prototype count; link | Facts + link. **Narrative not included.** |
| TVTropes | tvtropes.org | **URL + trope count only** | CC BY-NC-SA (non-commercial) — **text excluded.** |
| PriceCharting | pricecharting.com | Loose/CIB price, rarity tier; link | Facts + link. |
| gcmatome (ゲームカタログ@Wiki) | w.atwiki.jp/gcmatome | Quality **verdict** label; link | Label + link. **Body prose not included.** |
| VNDB | vndb.org | Tags, length, rating, popularity, titles, developers; link | **Database ODbL; contents DbCL — commercial use permitted** ([vndb.org/d17](https://vndb.org/d17)). Tag labels + numeric/title facts are included as DbCL contents. Only VNDB's *anime* data is CC BY-NC-SA (AniDB-sourced) and is **not** used here. `vndb_description` is dropped as editorial prose ("separate license conditions"). |
| refuge.tokyo | refuge.tokyo | Media label; link | Fact + link. **Writeups not included.** |
| gavas.jp | gavas.media | Sales rank, units, review count; link | Facts + link. **Reviews not included.** |
| GDRI | gdri.smspower.org | Studio names, categories, credits (facts); link | Facts + link. **Studio histories not included.** |
| Bahamut (巴哈姆特) | acg.gamer.com.tw | TW title, genre label; link | Facts + link. **Description not included.** |
| Chinese localization tracker | OldmanEmu / rendiyu | Localization status, titles, patch refs | Facts only. |
| Grospixels | grospixels.com | Article title/author/year (facts); link | Facts + link. **Body not included.** |

*(Sources marked "link only" or "X not included" contributed a `*_url` pointer and/or
factual fields, but their copyrighted prose is not part of this dataset.)*

## Database/compilation rights

The selection, arrangement, and the editorial layer (tags + descriptions) are the original
contribution of this project and are licensed CC BY-SA 4.0. Any EU *sui generis* database
right in the compilation is granted under the same license.

## A note on facts vs. terms of service

Several upstream sources (IGDB, MobyGames, LaunchBox, PriceCharting, and others) attach their
own Terms of Service to API/site access. This dataset reproduces only **uncopyrightable facts**
(numbers, dates, short labels) and **links** from those sources — it does **not** redistribute
their databases or prose, and it does **not** assert that any upstream ToS has been waived.
VNDB's data is open (database ODbL, contents DbCL — commercial use permitted); its tag labels are
included as DbCL contents and its prose `vndb_description` is dropped. The one genuinely
**non-commercial** source is **TVTropes (CC BY-NC-SA)** — its text is excluded entirely; only the
link and a numeric trope count remain.

## Corrections

Factual errors are inevitable in a corpus this size and this obscure. Corrections and
source pointers are welcome via the project repository.
