# Data Dictionary — PS1 Discovery Corpus

127 columns × 7,995 rows. Coverage = rows with a non-empty value. Columns that were empty across every row are omitted from the release; third-party editorial prose bodies are not redistributed (kept as their `*_url` pointer). See ATTRIBUTION.md for per-source licensing.

| # | Column | Type | Coverage | Source | Licensing | Description |
|---|--------|------|----------|--------|-----------|-------------|
| 0 | `title_en` | string | 7,995 (100%) | PSXDC / Wikipedia | Fact | Primary (English / Western) title. |
| 1 | `title_jp` | string | 3,243 (41%) | JA Wikipedia | Fact | Native Japanese-script title, where known. |
| 2 | `title_romaji` | string | 3,243 (41%) | derived | Fact | Romanized Japanese title. |
| 3 | `regions` | string | 7,995 (100%) | PSXDC + Wikipedia dates | Fact | Release regions present, comma-list of NTSC-U / NTSC-J / PAL. |
| 4 | `serial` | string | 7,995 (100%) | PSXDC | Fact | PlayStation disc serial (e.g. SLUS-00594). Wiki-only stubs carry a synthetic WK-/JK- id; see is_stub. |
| 5 | `year` | integer | 7,992 (99.9%) | PSXDC / Wikipedia | Fact | Release year (earliest known). |
| 6 | `developer` | string | 7,972 (99.7%) | PSXDC (Wikipedia fallback) | Fact | Developer studio. |
| 7 | `publisher` | string | 7,995 (100%) | PSXDC (Wikipedia fallback) | Fact | Publisher. |
| 8 | `curated_short_desc` | string | 7,995 (100%) | this project | Ours · CC BY-SA | Original one-paragraph description, written from each game's own evidence (never copied), adversarially verified. The primary search text. Covers 100% of rows. |
| 9 | `tags` | JSON object | 7,995 (100%) | this project | Ours · CC BY-SA | Controlled-vocabulary tags: a JSON object keyed by 10 dimensions (genre, mood, setting, mechanic, cultural_lineage, discovery, quality, difficulty, length, recommendation), each a list of tags from the 330-tag vocabulary. See TAG_VOCABULARY.md. |
| 10 | `is_stub` | boolean | 7,995 (100%) | this project | Ours · CC BY-SA | True for the 134 thin wiki-only stub rows (a real game with no PSXDC catalogue page); False for the 7,861 full PSXDC rows. |
| 11 | `psx_datacenter_link` | string | 7,995 (100%) | various | Fact |  |
| 12 | `wikipedia_url` | url | 2,590 (32%) | wikipedia | Fact | Link to the wikipedia page (pointer / attribution). |
| 13 | `jpwiki_url` | url | 1,091 (14%) | jpwiki | Fact | Link to the jpwiki page (pointer / attribution). |
| 14 | `wikidata_qid` | string | 3,461 (43%) | Wikidata | Wikidata · CC0 | Wikidata entity id (language-agnostic identity key, e.g. Q123456). |
| 15 | `mobygames_url` | url | 3,593 (45%) | mobygames | Fact | Link to the mobygames page (pointer / attribution). |
| 16 | `mobygames_score` | float | 2,259 (28%) | MobyGames | Fact | MobyScore (0–10). |
| 17 | `mobygames_genres` | string | 3,450 (43%) | MobyGames | Fact | Genre labels, comma-list. |
| 18 | `igdb_url` | url | 2,137 (27%) | igdb | Fact | Link to the igdb page (pointer / attribution). |
| 19 | `giantbomb_url` | url | 1,959 (25%) | giantbomb | Fact | Link to the giantbomb page (pointer / attribution). |
| 20 | `steam_url` | url | 168 (2%) | steam | Fact | Link to the steam page (pointer / attribution). |
| 21 | `official_url` | url | 612 (8%) | official | Fact | Link to the official page (pointer / attribution). |
| 22 | `community_video_url` | url | 1,858 (23%) | LaunchBox | Fact | Community gameplay video link (YouTube). |
| 23 | `wiki_extract` | string | 2,590 (32%) | EN Wikipedia | Wikipedia · CC BY-SA | English Wikipedia lead-summary extract. |
| 24 | `jpwiki_extract` | string | 1,091 (14%) | JA Wikipedia | Wikipedia · CC BY-SA | Japanese Wikipedia lead-summary extract. |
| 25 | `wiki_infobox_director` | string | 500 (6%) | EN Wikipedia | Wikipedia · CC BY-SA | Director(s) from the Wikipedia infobox. |
| 26 | `wiki_infobox_composer` | string | 883 (11%) | EN Wikipedia | Wikipedia · CC BY-SA | Composer(s) from the Wikipedia infobox. |
| 27 | `wiki_infobox_designer` | string | 592 (7%) | EN Wikipedia | Wikipedia · CC BY-SA | Designer(s) from the Wikipedia infobox. |
| 28 | `wiki_infobox_series` | string | 832 (10%) | EN Wikipedia | Wikipedia · CC BY-SA | Series from the Wikipedia infobox. |
| 29 | `wiki_infobox_modes` | string | 1,702 (21%) | EN Wikipedia | Wikipedia · CC BY-SA | Game modes from the Wikipedia infobox. |
| 30 | `community_rating` | float | 4,708 (59%) | LaunchBox | Fact | LaunchBox community rating (0–5). |
| 31 | `community_rating_count` | integer | 4,978 (62%) | LaunchBox | Fact | Number of LaunchBox ratings. |
| 32 | `popularity` | integer | 7,724 (97%) | Libretro | Fact | Libretro user count (popularity proxy). |
| 33 | `gamedb_genres` | string | 7,725 (97%) | GameDB-PSX | Fact | Genre labels, comma-list. |
| 34 | `igdb_themes` | string | 1,589 (20%) | IGDB | Fact | IGDB themes, comma-list (Fantasy, Horror, Sci-fi, …). |
| 35 | `igdb_perspectives` | string | 1,635 (20%) | IGDB | Fact | IGDB player perspectives, comma-list. |
| 36 | `igdb_game_modes` | string | 1,714 (21%) | IGDB | Fact | IGDB game modes, comma-list (Single player, Co-op, …). |
| 37 | `igdb_keywords` | string | 1,753 (22%) | IGDB | Fact | IGDB auto-tag keyword cloud, comma-list. |
| 38 | `igdb_similar_games` | JSON | 1,979 (25%) | IGDB | Fact | Related games as a JSON array of {name, slug} — semantic seeds. |
| 39 | `igdb_rating` | float | 1,206 (15%) | IGDB | Fact | IGDB total rating. |
| 40 | `igdb_rating_count` | integer | 1,206 (15%) | IGDB | Fact | IGDB total rating count. |
| 41 | `playtime_main_story` | float | 3,000 (38%) | HowLongToBeat | Fact | Main-story length, hours. |
| 42 | `playtime_main_extra` | float | 3,000 (38%) | HowLongToBeat | Fact | Main + extras length, hours. |
| 43 | `playtime_completionist` | float | 3,000 (38%) | HowLongToBeat | Fact | Completionist length, hours. |
| 44 | `hltb_url` | url | 3,000 (38%) | hltb | Fact | Link to the hltb page (pointer / attribution). |
| 45 | `hg101_url` | url | 538 (7%) | hg101 | Fact | Link to the hg101 page (pointer / attribution). |
| 46 | `budget_series_labels` | string | 1,297 (16%) | PSXDC / various | Fact | Budget-reissue series memberships, comma-list (e.g. Greatest Hits, PSone Books). |
| 47 | `speedrun_url` | url | 2,129 (27%) | speedrun | Fact | Link to the speedrun page (pointer / attribution). |
| 48 | `speedrun_category_count` | integer | 2,129 (27%) | Speedrun.com | Fact | Number of speedrun categories. |
| 49 | `speedrun_runs_count` | integer | 2,129 (27%) | Speedrun.com | Fact | Number of verified runs. |
| 50 | `retroachievements_url` | url | 1,488 (19%) | retroachievements | Fact | Link to the retroachievements page (pointer / attribution). |
| 51 | `retroachievements_achievement_count` | integer | 1,488 (19%) | RetroAchievements | Fact | Number of achievements defined. |
| 52 | `retroachievements_players_total` | integer | 1,488 (19%) | RetroAchievements | Fact | Total players tracked. |
| 53 | `hiddenpalace_url` | url | 943 (12%) | hiddenpalace | Fact | Link to the hiddenpalace page (pointer / attribution). |
| 54 | `hiddenpalace_prototype_count` | integer | 943 (12%) | Hidden Palace | Fact | Number of archived prototype/dev builds. |
| 55 | `tvtropes_url` | url | 1,392 (17%) | tvtropes | Fact | Link to the tvtropes page (pointer / attribution). |
| 56 | `tvtropes_trope_count` | integer | 1,392 (17%) | TVTropes | Fact | Number of tropes catalogued (count only; trope text is not redistributed — CC-BY-NC-SA). |
| 57 | `pricecharting_url` | url | 1,726 (22%) | pricecharting | Fact | Link to the pricecharting page (pointer / attribution). |
| 58 | `pricecharting_loose_price_usd` | float | 1,588 (20%) | PriceCharting | Fact | Secondhand loose price, USD. |
| 59 | `pricecharting_cib_price_usd` | float | 1,700 (21%) | PriceCharting | Fact | Secondhand complete-in-box price, USD. |
| 60 | `pricecharting_rarity_tier` | string | 1,700 (21%) | PriceCharting | Fact | Rarity tier label. |
| 61 | `bahamut_url` | url | 111 (1%) | bahamut | Fact | Link to the bahamut page (pointer / attribution). |
| 62 | `bahamut_title` | string | 111 (1%) | Bahamut (TW) | Fact | Traditional-Chinese title. |
| 63 | `bahamut_genre` | string | 111 (1%) | Bahamut (TW) | Fact | Genre label (zh-TW). |
| 64 | `chinese_localization_status` | string | 6 (<0.1%) | CN localization tracker | Fact | official / fan / both. |
| 65 | `chinese_localization_titles` | string | 6 (<0.1%) | CN localization tracker | Fact | Chinese title(s). |
| 66 | `chinese_localization_sources` | string | 6 (<0.1%) | CN localization tracker | Fact | Source references for the localization. |
| 67 | `chinese_localization_patches` | string | 6 (<0.1%) | CN localization tracker | Fact | Fan-translation patch references. |
| 68 | `gdri_developer_url` | url | 1,500 (19%) | gdri developer | Fact | Link to the gdri developer page (pointer / attribution). |
| 69 | `gdri_developer_title` | string | 1,500 (19%) | GDRI | Fact | Developer studio name (GDRI canonical). |
| 70 | `gdri_developer_jp_name` | string | 964 (12%) | GDRI | Fact | Developer name in Japanese. |
| 71 | `gdri_developer_categories` | string | 1,235 (15%) | GDRI | Fact | Studio category labels, comma-list. |
| 72 | `gdri_devs_all_json` | JSON | 27 (0.3%) | GDRI | Fact | Per-game credited developers/roles as JSON (names = facts). |
| 73 | `gavas_url` | url | 31 (0.4%) | gavas | Fact | Link to the gavas page (pointer / attribution). |
| 74 | `gavas_sales_rank` | integer | 31 (0.4%) | gavas.jp | Fact | Japanese sales rank. |
| 75 | `gavas_sales_units_million` | float | 31 (0.4%) | gavas.jp | Fact | Reported sales, millions of units. |
| 76 | `gavas_user_review_count` | integer | 31 (0.4%) | gavas.jp | Fact | Number of user reviews. |
| 77 | `refugetokyo_url` | url | 2,218 (28%) | refugetokyo | Fact | Link to the refugetokyo page (pointer / attribution). |
| 78 | `refugetokyo_media` | string | 3 (<0.1%) | refuge.tokyo | Fact | Media/format label. |
| 79 | `vndb_url` | url | 215 (3%) | vndb | Fact | Link to the vndb page (pointer / attribution). |
| 80 | `vndb_title` | string | 215 (3%) | VNDB | Fact | Visual-novel title (VNDB). |
| 81 | `vndb_alttitle` | string | 207 (3%) | VNDB | Fact | Japanese VN title. |
| 82 | `vndb_length` | integer | 63 (0.8%) | VNDB | Fact | Length bucket 1–5 (very short → very long). |
| 83 | `vndb_length_minutes` | integer | 49 (0.6%) | VNDB | Fact | Estimated length, minutes. |
| 84 | `vndb_rating` | float | 65 (0.8%) | VNDB | Fact | VNDB rating (0–100). |
| 85 | `vndb_popularity` | float | 215 (3%) | VNDB | Fact | VNDB popularity (0–10). |
| 86 | `vndb_tags` | string | 204 (3%) | VNDB | Fact | VNDB tag labels, comma-list (VNDB contents are DbCL — commercial-OK; see ATTRIBUTION.md). |
| 87 | `vndb_developers` | string | 208 (3%) | VNDB | Fact | VN developers, comma-list. |
| 88 | `gcmatome_url` | url | 580 (7%) | gcmatome | Fact | Link to the gcmatome page (pointer / attribution). |
| 89 | `gcmatome_verdict` | string | 579 (7%) | gcmatome (JA) | Fact | Japanese community quality verdict (良作 / クソゲー / スルメゲー …) — a search facet. |
| 90 | `frwiki_url` | url | 2,113 (26%) | French Wikipedia | Fact | French Wikipedia article URL. |
| 91 | `frwiki_title` | string | 2,113 (26%) | French Wikipedia | Wikipedia · CC BY-SA | French Wikipedia article title. |
| 92 | `frwiki_extract` | string | 2,094 (26%) | French Wikipedia | Wikipedia · CC BY-SA | French Wikipedia lead-summary extract. |
| 93 | `frwiki_categories` | string | 2,064 (26%) | French Wikipedia | Wikipedia · CC BY-SA | French Wikipedia categories, comma-list. |
| 94 | `grospixels_url` | url | 147 (2%) | grospixels | Fact | Link to the grospixels page (pointer / attribution). |
| 95 | `grospixels_title` | string | 147 (2%) | Grospixels | Fact | Article title. |
| 96 | `grospixels_author` | string | 147 (2%) | Grospixels | Fact | Article author (attribution). |
| 97 | `grospixels_year` | integer | 147 (2%) | Grospixels | Fact | Article year. |
| 98 | `dewiki_url` | url | 885 (11%) | German Wikipedia | Fact | German Wikipedia article URL. |
| 99 | `dewiki_title` | string | 885 (11%) | German Wikipedia | Wikipedia · CC BY-SA | German Wikipedia article title. |
| 100 | `dewiki_extract` | string | 885 (11%) | German Wikipedia | Wikipedia · CC BY-SA | German Wikipedia lead-summary extract. |
| 101 | `dewiki_categories` | string | 885 (11%) | German Wikipedia | Wikipedia · CC BY-SA | German Wikipedia categories, comma-list. |
| 102 | `itwiki_url` | url | 1,744 (22%) | Italian Wikipedia | Fact | Italian Wikipedia article URL. |
| 103 | `itwiki_title` | string | 1,744 (22%) | Italian Wikipedia | Wikipedia · CC BY-SA | Italian Wikipedia article title. |
| 104 | `itwiki_extract` | string | 1,679 (21%) | Italian Wikipedia | Wikipedia · CC BY-SA | Italian Wikipedia lead-summary extract. |
| 105 | `itwiki_categories` | string | 1,744 (22%) | Italian Wikipedia | Wikipedia · CC BY-SA | Italian Wikipedia categories, comma-list. |
| 106 | `eswiki_url` | url | 1,570 (20%) | Spanish Wikipedia | Fact | Spanish Wikipedia article URL. |
| 107 | `eswiki_title` | string | 1,570 (20%) | Spanish Wikipedia | Wikipedia · CC BY-SA | Spanish Wikipedia article title. |
| 108 | `eswiki_extract` | string | 1,568 (20%) | Spanish Wikipedia | Wikipedia · CC BY-SA | Spanish Wikipedia lead-summary extract. |
| 109 | `eswiki_categories` | string | 1,570 (20%) | Spanish Wikipedia | Wikipedia · CC BY-SA | Spanish Wikipedia categories, comma-list. |
| 110 | `kowiki_url` | url | 943 (12%) | Korean Wikipedia | Fact | Korean Wikipedia article URL. |
| 111 | `kowiki_title` | string | 943 (12%) | Korean Wikipedia | Wikipedia · CC BY-SA | Korean Wikipedia article title. |
| 112 | `kowiki_extract` | string | 941 (12%) | Korean Wikipedia | Wikipedia · CC BY-SA | Korean Wikipedia lead-summary extract. |
| 113 | `kowiki_categories` | string | 943 (12%) | Korean Wikipedia | Wikipedia · CC BY-SA | Korean Wikipedia categories, comma-list. |
| 114 | `ruwiki_url` | url | 1,252 (16%) | Russian Wikipedia | Fact | Russian Wikipedia article URL. |
| 115 | `ruwiki_title` | string | 1,252 (16%) | Russian Wikipedia | Wikipedia · CC BY-SA | Russian Wikipedia article title. |
| 116 | `ruwiki_extract` | string | 1,252 (16%) | Russian Wikipedia | Wikipedia · CC BY-SA | Russian Wikipedia lead-summary extract. |
| 117 | `ruwiki_categories` | string | 1,252 (16%) | Russian Wikipedia | Wikipedia · CC BY-SA | Russian Wikipedia categories, comma-list. |
| 118 | `ptwiki_url` | url | 1,113 (14%) | Portuguese Wikipedia | Fact | Portuguese Wikipedia article URL. |
| 119 | `ptwiki_title` | string | 1,113 (14%) | Portuguese Wikipedia | Wikipedia · CC BY-SA | Portuguese Wikipedia article title. |
| 120 | `ptwiki_extract` | string | 1,110 (14%) | Portuguese Wikipedia | Wikipedia · CC BY-SA | Portuguese Wikipedia lead-summary extract. |
| 121 | `ptwiki_categories` | string | 1,113 (14%) | Portuguese Wikipedia | Wikipedia · CC BY-SA | Portuguese Wikipedia categories, comma-list. |
| 122 | `plwiki_url` | url | 757 (9%) | Polish Wikipedia | Fact | Polish Wikipedia article URL. |
| 123 | `plwiki_title` | string | 757 (9%) | Polish Wikipedia | Wikipedia · CC BY-SA | Polish Wikipedia article title. |
| 124 | `plwiki_extract` | string | 751 (9%) | Polish Wikipedia | Wikipedia · CC BY-SA | Polish Wikipedia lead-summary extract. |
| 125 | `plwiki_categories` | string | 757 (9%) | Polish Wikipedia | Wikipedia · CC BY-SA | Polish Wikipedia categories, comma-list. |
| 126 | `sources` | string | 7,995 (100%) | this project | Fact | Provenance: comma-list of which sources contributed to this row. |

## Sparsest columns (<1% coverage — treat as anecdotal)

These columns are present but populated on very few rows; don't build core logic on them:

`refugetokyo_media` (3), `chinese_localization_status` (6), `chinese_localization_titles` (6), `chinese_localization_sources` (6), `chinese_localization_patches` (6), `gdri_devs_all_json` (27), `gavas_url` (31), `gavas_sales_rank` (31), `gavas_sales_units_million` (31), `gavas_user_review_count` (31), `vndb_length_minutes` (49), `vndb_length` (63), `vndb_rating` (65)

## Licensing rollup (by column count)

- **Facts — public domain** — 92 columns
- **Wikipedia — CC BY-SA 4.0** — 31 columns
- **Our editorial — CC BY-SA 4.0** — 3 columns
- **Wikidata — CC0** — 1 columns
