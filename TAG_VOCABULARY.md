# Tag Vocabulary — PS1 Discovery Corpus

**330 tags across 10 orthogonal dimensions.** Each game receives 15-25 tags. The `tags` column in the dataset is a JSON object keyed by these dimension names, each holding a list of the tags that apply. The machine-readable source of truth is `tag_vocabulary.json` (shipped alongside).

> Controlled vocabulary for the editorial pass. Each PS1 game should receive 15-25 tags across 10 orthogonal dimensions. A game can be 'JRPG' (genre) + 'Dark' (mood) + 'Cyberpunk' (setting) + 'Turn-Based' (mechanic) + 'Anime-Aesthetic' (cultural_lineage) + 'Cult-Classic' (discovery) + 'Quality-Strong' (quality) + 'Difficulty-Hard' (difficulty) + 'Length-Epic' (length) + 'Recommended-For-Genre-Fans' (recommendation). The vocabulary is broad enough that a semantic-search query like 'cozy farming sim with anime aesthetic' maps cleanly, narrow enough that every tag has meaningful population.

**Realized vs. allowed:** the vocabulary is the controlled *allowed* set. In this snapshot **310 of 330** tags are actually used; the remaining **20** have zero population (a tag-filter UI built straight from the vocab would render 20 always-empty facets).

## genre  (69 tags)

_What kind of game it is — the primary form. Mostly one or two tags per game._

`Action`, `Action-Adventure`, `Adventure`, `Point-and-Click-Adventure`, `Platformer-2D`, `Platformer-3D`, `Run-and-Gun`, `Shooter-First-Person`, `Shooter-Third-Person`, `Shooter-Rail`, `Shooter-Light-Gun`, `Shoot-em-Up`, `JRPG`, `WRPG`, `Action-RPG`, `Tactical-RPG`, `Dungeon-Crawler`, `Fighting-2D`, `Fighting-3D`, `Beat-em-Up`, `Wrestling`, `Racing-Arcade`, `Racing-Sim`, `Kart-Racing`, `Combat-Racing`, `Sports-Soccer`, `Sports-Basketball`, `Sports-Baseball`, `Sports-Golf`, `Sports-Tennis`, `Sports-Other`, `Snowboarding`, `Skateboarding`, `Fishing`, `Puzzle`, `Puzzle-Block-Falling`, `Puzzle-Logic`, `Puzzle-Word`, `Strategy-Real-Time`, `Strategy-Turn-Based`, `Wargame`, `Simulation-Life`, `Simulation-Vehicle`, `Simulation-City-Building`, `Simulation-Train`, `Simulation-Pet`, `Simulation-God`, `Simulation-Farm`, `Visual-Novel`, `Sound-Novel`, `Dating-Sim`, `Otome`, `Survival-Horror`, `Stealth`, `Rhythm-Dance`, `Rhythm-Karaoke`, `Rhythm-DJ`, `Music-Game`, `Educational`, `Edutainment`, `Kids`, `Quiz-Trivia`, `Party-Mini-Game`, `Board-Game`, `Card-Game`, `Mahjong`, `Pachinko-Pachislot`, `Casino-Gambling`, `Compilation`

## mood  (48 tags)

_How the game FEELS. Atmospheric / emotional register. Usually 1-3 tags per game. This is the dimension a semantic-search query like 'something melancholy and beautiful' matches into._

`Dark`, `Bleak`, `Melancholic`, `Tragic`, `Brooding`, `Gothic`, `Comedic`, `Whimsical`, `Lighthearted`, `Slapstick`, `Cute`, `Charming`, `Cozy`, `Wholesome`, `Surreal`, `Dreamlike`, `Trippy`, `Bizarre`, `Avant-Garde`, `Pulpy`, `Cult-Trashy`, `B-Movie`, `Tense`, `Suspenseful`, `Claustrophobic`, `Paranoid`, `Atmospheric`, `Meditative`, `Contemplative`, `Triumphant`, `Heroic`, `Inspiring`, `Earnest`, `Sincere`, `Edgy`, `Transgressive`, `Provocative`, `Gritty`, `Realistic-Tone`, `Grounded`, `Mysterious`, `Enigmatic`, `Erotic`, `Sexually-Charged`, `Otaku-Coded`, `Niche-Otaku`, `Nostalgic`, `Wistful`

## setting  (53 tags)

_Where + when. Often 1-3 tags per game._

`Fantasy-High`, `Fantasy-Low`, `Fantasy-Dark`, `Fantasy-Urban`, `Sci-Fi-Hard`, `Sci-Fi-Space-Opera`, `Cyberpunk`, `Post-Apocalyptic`, `Dystopian`, `Bio-Punk`, `Steampunk`, `Modern-Day`, `Contemporary-Urban`, `Suburban`, `Rural`, `Historical-Medieval`, `Historical-Renaissance`, `Historical-Victorian`, `Historical-WW1`, `Historical-WW2`, `Historical-Cold-War`, `Historical-Edo`, `Historical-Sengoku`, `Historical-Bakumatsu`, `Historical-Wild-West`, `Historical-Ancient`, `Mythological-Greek`, `Mythological-Norse`, `Mythological-Japanese`, `Mythological-Chinese`, `Mythological-Egyptian`, `Mythological-Hindu`, `School-Setting`, `Magical-Academy`, `Military-Theater`, `Naval`, `Aerial`, `Crime-Noir`, `Yakuza-Underworld`, `Mafia-Underworld`, `Underwater`, `Outer-Space`, `Spaceship-Interior`, `Otherworldly-Spirit`, `Cyberspace`, `Virtual-Reality`, `Sports-Stadium`, `Racetrack`, `Real-World-Japan`, `Real-World-North-America`, `Real-World-Europe`, `Prehistoric`, `Lovecraftian`

## mechanic  (50 tags)

_How you actually play. 2-5 tags per game._

`Perspective-First-Person`, `Perspective-Third-Person`, `Perspective-Top-Down`, `Perspective-Side-Scrolling`, `Perspective-Isometric`, `Perspective-2.5D`, `Turn-Based`, `Real-Time`, `Active-Time-Battle`, `Single-Player`, `Multiplayer-Local`, `Co-op-Local`, `Split-Screen`, `Hotseat`, `Link-Cable-Multiplayer`, `Branching-Narrative`, `Multiple-Endings`, `Linear-Narrative`, `Open-World`, `Sandbox`, `Hub-World`, `Linear-Levels`, `Stage-Based-Levels`, `Permadeath`, `Procedural-Generation`, `Crafting`, `Inventory-Management`, `Resource-Management`, `Cover-Based`, `Combo-Based`, `Quick-Time-Events`, `Grid-Tactics`, `Polygonal-3D`, `Pre-Rendered-Backgrounds`, `Sprite-Based`, `FMV-Heavy`, `Hand-Drawn`, `Light-Gun-Compatible`, `Steering-Wheel-Compatible`, `Dance-Pad-Compatible`, `Mouse-Compatible`, `Multitap-Compatible`, `Vibration-Compatible`, `Analog-Required`, `Save-Point`, `Save-Anywhere`, `Password-System`, `Memory-Card-Heavy`, `New-Game-Plus`, `Postgame-Content`

## cultural_lineage  (34 tags)

_Where the game's design DNA comes from. Often 1-2 tags. Useful for queries like 'classic JRPG vibe' or 'Western action with anime aesthetic'._

`Japanese-Design`, `Western-Design`, `Korean-Design`, `Chinese-Design`, `Anime-Aesthetic`, `Manga-Inspired`, `Bishoujo`, `Bishonen`, `Otome-Aesthetic`, `Mecha-Genre`, `Magical-Girl`, `Realistic-Western-Aesthetic`, `Cartoon-Western-Aesthetic`, `Photoreal`, `Stylized-Western`, `Wuxia`, `K-Drama-Tone`, `Cel-Shaded`, `Pixel-Art`, `Low-Poly-Aesthetic`, `Hand-Crafted-Look`, `Anime-Tie-In`, `Manga-Tie-In`, `TV-Show-Tie-In`, `Film-Tie-In`, `Comic-Tie-In`, `Novel-Adaptation`, `Disney-Tie-In`, `Pixar-Tie-In`, `Nickelodeon-Tie-In`, `Sports-License`, `Athlete-License`, `Celebrity-License`, `Music-Artist-License`

## discovery  (47 tags)

_The 'how does someone find this' axis — the project-defining dimension. Many games carry 2-4 tags here. Captures regional exclusivity, translation status, cult/mainstream, format._

`Japan-Exclusive`, `NA-Exclusive`, `PAL-Exclusive`, `Multi-Region`, `Officially-Localized-EN`, `Officially-Localized-FR`, `Officially-Localized-DE`, `Officially-Localized-IT`, `Officially-Localized-ES`, `Officially-Localized-PT`, `Officially-Localized-KO`, `Officially-Localized-CN`, `Officially-Localized-RU`, `Fan-Translated-EN`, `Fan-Translated-CN`, `Fan-Translated-Other`, `Cancelled`, `Prototype-Only`, `Beta-Only`, `Unreleased`, `Lost-Media`, `Cult-Classic`, `Hidden-Gem`, `Underappreciated`, `Mainstream-Hit`, `Console-Defining`, `Obscure`, `Truly-Obscure`, `Genre-Defining`, `Genre-Bending`, `Series-Starter`, `Series-Entry-Late`, `Budget-Reissue`, `Greatest-Hits-NA`, `Platinum-PAL`, `PSone-Books-JP`, `The-Best-JP`, `PSone-Classics-PSN`, `Single-Disc`, `Two-Disc`, `Three-Disc`, `Multi-Disc-Epic`, `Four-Plus-Disc`, `Demo-Disc-Inclusion`, `Promotional-Pack-In`, `Speedrun-Active-Community`, `RetroAchievement-Active`

## quality  (15 tags)

_Editorial opinion on overall quality + reputation + how the game holds up today. Usually 1-3 tags per game. Curiosity-* tags handle the 'bad but worth playing' case explicitly so we don't have to compress into a single low score._

`Quality-Essential`, `Quality-Classic`, `Quality-Strong`, `Quality-Good`, `Quality-Mediocre`, `Quality-Bad`, `Quality-Broken`, `Curiosity-Bad-But-Interesting`, `Curiosity-So-Bad-Its-Good`, `Curiosity-Misunderstood`, `Underrated`, `Overrated`, `Aged-Well`, `Aged-Poorly`, `Aged-Charmingly`

## difficulty  (4 tags)

_How hard the game plays. Usually exactly 1 tag per game._

`Difficulty-Casual`, `Difficulty-Standard`, `Difficulty-Hard`, `Difficulty-Punishing`

## length  (5 tags)

_Typical playtime to complete a primary run. Usually exactly 1 tag per game._

`Length-Short`, `Length-Medium`, `Length-Long`, `Length-Epic`, `Length-Endless`

## recommendation  (5 tags)

_Which audience profile gets the most out of this game. Multi-valued — a game can be both 'For-Beginners' and 'For-Genre-Fans'._

`Recommended-For-Beginners`, `Recommended-For-Genre-Fans`, `Recommended-For-Completionists`, `Recommended-For-Historians`, `Recommended-For-Speedrunners`
