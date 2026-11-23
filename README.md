# Pokémon Crystal Complete

**Pokémon Crystal Complete** is an in-progress, single-player-friendly ROM hack based on the [pret/pokecrystal][upstream] disassembly of Pokémon Crystal.

The goal is to preserve the charm and identity of Generation II while making Pokémon Crystal more complete, convenient, balanced, and self-contained.

The project focuses on improved Pokémon availability, modernized battle mechanics, alternative evolution methods, restored events, updated movesets, and quality-of-life improvements.

Development is organized into small, testable milestones. Features are added gradually and tested before releases.

> **Development status:** Early development and testing. The roadmap describes both implemented and planned features. Features listed below should not be assumed complete unless explicitly identified as implemented and tested.

## Project goals

- Make most original Generation I and II Pokémon obtainable naturally in a single save file, with the long-term goal of all 251.
- Remove version-exclusive restrictions.
- Provide alternatives to trade evolutions.
- Restore missing and event-exclusive content, including the GS Ball/Celebi event.
- Modernize experience distribution, moves, types, evolution methods, and selected battle mechanics.
- Improve encounter variety, trainer teams, and the level curve throughout Johto and Kanto.
- Add reusable TMs and reduce unnecessary HM restrictions.
- Improve shops, items, gifts, and NPC rewards.
- Remove obsolete multiplayer and communication systems in a later update.
- Add Normal and Challenge difficulty options.
- Preserve the atmosphere and identity of the original Pokémon Crystal.

## Pokémon availability

The long-term goal is to make all 251 original Pokémon obtainable without requiring a second game, external trading, Mystery Gift, or time-limited distributions.

**Version 1 will not claim complete Pokédex availability.**

Most Generation I and II Pokémon are intended to be obtainable, but some legendary or mythical encounters and species associated with restored Kanto locations may remain unavailable until later versions.

Additional encounters will be introduced progressively, with Pokémon placed in locations appropriate to their species.

Examples include:

- Moving late-game Johto species into suitable Johto locations.
- Making Houndour, Murkrow, Larvitar, and other Johto Pokémon accessible earlier.
- Adding Horsea to Good Rod encounters before Clair.
- Expanding Headbutt, fishing, and Bug-Catching Contest encounters.
- Introducing Kanto starters in wild locations inspired by *Pokémon: Let's Go, Pikachu!* and *Let's Go, Eevee!*.
- Relocating Pokémon associated with inaccessible original Kanto areas until those maps are restored.
- Restoring special encounters and legendary events over subsequent versions.

A future availability audit will document each Pokémon's location, encounter method, time restrictions, and version requirements.

## Development and testing

Changes are developed and tested in manageable chunks.

- Keep releases separate from development milestones.
- Test new features before marking them complete.
- Use fresh-save playthroughs for major gameplay and save-structure changes.
- Track bugs, implementation work, and regression tests through GitHub Issues.
- Avoid distributing copyrighted game ROMs; distribute patches and project source code instead.
- Keep the README updated as implementation progresses.

### Current implementation status

The following foundations have been committed to the repository:

- Initial upstream synchronization and local build setup.
- Fairy-type groundwork, including type data, selected moves, and Pokémon typings.
- Corrected Normal/Fairy typing for Wigglytuff.
- Reworked EXP Share as a toggleable Key Item.
- Added experience gain from catching Pokémon.
- Added Horsea to Good Rod encounters.
- Updated Remoraid fishing encounters.
- Expanded the Bug-Catching Contest with more Generation II Pokémon.
- Updated selected Johto and Kanto wild encounters.
- Expanded some Headbutt encounter groups.
- Updated the in-game Onix trade so Rocky holds Metal Coat.
- Changed the Lottery Corner's former EXP Share prize to Lucky Egg.

These changes require continued gameplay verification before being considered fully complete.

### Test teams

**Milestone 1 regression team**

- Steelix
- Typhlosion
- Togetic
- Ampharos
- Girafarig
- Poliwag

**Evolution and gameplay test team**

- Umbreon
- Typhlosion
- Lapras
- Wigglytuff
- Scizor
- Victreebel

Test teams may change as new features are implemented.

---

# Release roadmap

The project is divided into the main **Classic Edition** releases, beginning with Version 1 and continuing through Version 8.

Version 1 contains several smaller GitHub milestones. Version 1.5 is a separate structural cleanup release.

The roadmap is subject to adjustment based on testing, available memory, and implementation complexity.

## Version 1 — Core modernization

**Goal:** Build a stable, modernized Pokémon Crystal with improved Pokémon availability, evolution methods, quality-of-life systems, and battle mechanics.

Version 1 is divided into seven development milestones.

### Milestone 0 — Repository setup

**Status: Completed**

- Synchronize with upstream `pret/pokecrystal`.
- Confirm a successful local build.
- Establish the development repository.
- Organize the initial roadmap and testing process.

### Milestone 1 — Pokédex and mechanics foundation

**Status: Code committed; regression testing in progress**

This milestone verifies the initial encounter, Fairy-type, and experience-system changes.

#### Encounter changes

- Remove selected version-exclusive restrictions.
- Improve Johto Pokémon availability.
- Add Houndour, Murkrow, Mareep, and other species to suitable earlier locations.
- Add Horsea to Good Rod encounters.
- Improve Remoraid fishing groups.
- Replace selected Bug-Catching Contest encounters with Generation II Pokémon.
- Expand Headbutt encounters.
- Add selected missing Kanto Pokémon to existing locations.

#### Mechanics

- Add Fairy-type groundwork.
- Update selected Pokémon to their modern Fairy typings.
- Update selected Fairy-type moves and type interactions.
- Rework EXP Share into a toggleable Key Item.
- Add catching experience.
- Update Rocky's held item to Metal Coat.

#### Testing

- Verify the revised wild encounter tables.
- Test Bug-Catching Contest and fishing encounters.
- Test EXP Share with the setting enabled and disabled.
- Test catching experience, including level-ups and move learning.
- Verify Fairy-type interactions.
- Test Rocky's in-game trade.
- Verify Mew and Celebi's existing Pokédex data.
- Perform a fresh-save regression playthrough.

Track progress using the [Milestone 1 GitHub Issues](https://github.com/jennifert/pokecrystal/issues?q=is%3Aopen%20milestone%3A%22Milestone%201%22).

### Milestone 2 — Evolution and trade fixes

**Status: Planned; Dragon Scale changes under initial testing**

Remove external trade requirements from evolution methods.

#### Link Cable evolutions

Introduce a Link Cable item for Pokémon that normally evolve through trading:

- Kadabra → Alakazam
- Machoke → Machamp
- Graveler → Golem
- Haunter → Gengar

#### Direct item evolutions

Allow evolution items to be used directly from the Bag, similarly to evolution stones:

- Poliwhirl + King's Rock → Politoed
- Slowpoke + King's Rock → Slowking
- Scyther + Metal Coat → Scizor
- Onix + Metal Coat → Steelix
- Seadra + Dragon Scale → Kingdra
- Porygon + Up-Grade → Porygon2

Dragon Scale is the initial test case.

Horsea should evolve into Seadra at Level 32, after which Dragon Scale can evolve Seadra directly into Kingdra without trading.

Dragon Scale must be obtainable before challenging Clair.

#### Evolution-item merchant

Add an evolution-item shop in Blackthorn City, accessible immediately upon reaching the city.

Planned inventory:

- Fire Stone
- Water Stone
- Thunderstone
- Leaf Stone
- Moon Stone
- Sun Stone
- King's Rock
- Metal Coat
- Dragon Scale
- Up-Grade
- Link Cable

#### NPC trades

Review and improve existing in-game trades.

- Preserve Rocky's Metal Coat.
- Reconsider the Olivine Voltorb trade.
- Review the Pewter Xatu trade.
- Review the Power Plant Magneton trade.
- Reconsider the Route 14 Aerodactyl trade.
- Consider additional opportunities to obtain the unchosen Johto starters.

All new evolution methods must be tested for item consumption, Pokédex registration, move learning, and save compatibility.

### Milestone 3 — Core quality-of-life improvements

**Status: Planned**

Implement essential gameplay conveniences.

- Infinitely reusable TMs.
- Display move names when receiving or purchasing TMs and HMs.
- Allow Pokémon to use field moves they are capable of learning without occupying a move slot, while preserving progression requirements.
- Add Running Shoes.
- Add a free Move Relearner near the Move Deleter in Blackthorn City.
- Remove overworld poison damage.
- Prevent unnecessary EXP gain calculations at Level 100.
- Make essential evolution and training items more accessible.

The Pocket PC, expanded Options interface, and other significant menu changes are reserved for Version 1.5.

### Milestone 4 — Moves and battle mechanics

**Status: Planned**

Modernize the original Pokémon's movesets and selected battle mechanics.

#### Move updates

Review:

- Move power and accuracy.
- PP values.
- Move typing.
- Level-up learnsets.
- Egg Moves.
- TM/HM compatibility.
- Evolution moves.
- Species-specific move availability.

Potential new or repurposed moves include:

- Sticky Web, replacing Spider Web.
- Facade, proposed as a replacement for Fury Swipes.
- Fury Attack replacement, still undecided.
- Scale Shot.
- Drain Punch.
- Water Pulse.
- Magnet Rise.
- Aerial Ace.
- Dual Wingbeat.
- Flip Turn.
- Volt Switch.

Modernize existing moves such as Fury Cutter, Leech Life, and other outdated attacks.

Keep Mean Look as a trapping move.

New move effects require separate testing and must fit within the available move slots.

#### Battle mechanics

- Complete the modern Fairy-type chart.
- Update outdated Ghost and Dark interactions against Steel.
- Correct the Dragon Fang and Dragon Scale type-boost behaviour.
- Modernize sleep and thaw mechanics.
- Reduce confusion's self-hit probability.
- Fix Steel-type poisoning from Twineedle.
- Add appropriate Grass-type immunities to powder-based moves.
- Add evolution moves.
- Review other documented Generation II battle-mechanics bugs.

Weather modernization is reserved for Version 8.

### Milestone 5 — Events and Pokémon availability

**Status: Planned**

Restore essential standalone events and expand Pokémon availability.

#### Celebi

Restore the GS Ball/Celebi event using the pret wiki implementation as a foundation.

- Make the event accessible through ordinary gameplay.
- Remove its dependency on external distribution or mobile communication.
- Preserve the GS Ball and Ilex Forest event sequence.
- Test the encounter, capture, Pokédex registration, and event flags.
- Ensure the event remains functional after Version 1.5's communication-system cleanup.

#### Additional availability

- Add Kanto starter encounters to suitable existing maps.
- Expand access to missing nonlegendary Pokémon.
- Review species previously restricted to inaccessible locations.
- Improve fossil Pokémon availability.
- Introduce selected legendary encounters where feasible.
- Allow missed or defeated stationary legendaries to be challenged again after suitable League progression.

The Mew truck event and larger restored Kanto areas are planned for later releases.

### Milestone 6 — Trainers and world balance

**Status: Planned**

Improve the original Normal Mode experience.

- Rework Johto Gym Leader teams.
- Review Kanto Gym Leader teams.
- Improve ordinary trainer Pokémon variety.
- Reduce repetitive Pidgey, Spearow, Caterpie, Weedle, and similar teams.
- Add more varied Bug-type teams, including appropriate evolved Pokémon.
- Improve Team Rocket's Pokémon variety.
- Adjust trainer levels to match the intended level curve.
- Improve encounter rarity and availability.
- Review item and money rewards.
- Improve shiny availability where appropriate.
- Revisit Red Gyarados's fixed DVs.
- Improve swarms and encounter diversity.

The full six-Pokémon Challenge Mode teams and advanced difficulty features will be introduced in Version 3.

### Milestone 7 — Version 1 release testing

**Status: Planned**

Complete a fresh-save playthrough and verify the Version 1 feature set.

- Complete Johto and Kanto.
- Verify normal progression and story events.
- Test the new evolution methods.
- Verify Pokémon availability and encounter tables.
- Test all core quality-of-life systems.
- Test new moves and revised type matchups.
- Test Celebi's restored event.
- Test save/load functionality.
- Review unexpected softlocks and event conflicts.
- Document unavailable species and features deferred to later releases.
- Update the README and release notes.

**Version 1 will be considered ready when its included features are stable and tested, not when all future planned Pokémon and content have been added.**

---

## Version 1.5 — Legacy cleanup and Options foundations

**Status: Planned**

Version 1.5 will remove obsolete communication functionality and establish the Options and save-data foundations needed for later updates.

### Remove obsolete systems

- Pokémon Center upper floors and their inaccessible communication facilities.
- Link trading and link battles.
- Time Capsule.
- Infrared Mystery Gift.
- Game Boy Printer functionality.
- Mail items, Mail writing, and mailbox functionality.
- Unneeded Mobile Adapter functions.
- Obsolete menus and dialogue associated with removed systems.

Preserve:

- Pokémon storage PCs.
- Pokégear phone calls.
- Trainer rematches and swarm contacts.
- In-game NPC trades.
- Pokémon breeding and Eggs.
- Battle Tower single-player content.
- GS Ball/Celebi and other single-player events.
- Useful decorations and rewards previously associated with Mystery Gift.

### Bill's Ecruteak City event

Replace Bill's original Time Capsule introduction.

Bill will appear beside the first-floor Pokémon Center PC in Ecruteak City.

His new story involves someone attempting to interfere with the Pokémon Storage System and leaving an Eevee behind.

Bill offers the player the abandoned Eevee, associated with a Friend Ball and high starting friendship.

Actual Poké Ball-origin tracking would require additional Pokémon data changes; the Friend Ball may initially be represented through dialogue.

Remove or replace the original duplicate Eevee gift event in Goldenrod.

### Kenya's redesigned quest

Remove the requirement to carry written Mail.

Replace the existing Route 35 delivery quest with event flags and new dialogue.

Planned reward:

- A permanent Level 21 Spearow named Kenya.
- Excellent fixed DVs, particularly Attack and Speed.
- Holds an HP Up.
- Optional special Egg Move, such as Tri Attack.
- New dialogue explaining Kenya's connection with the player.

Preserve or relocate the original TM50 Nightmare reward.

### Mystery Gift decorations

Redistribute former Mystery Gift decorations to ordinary gameplay.

Potential sources:

- Existing NPCs.
- Mahogany Town shop.
- Goldenrod and Celadon merchants.
- Optional gifts and exploration rewards.

### Options menu and save foundations

Introduce a visible difficulty setting:

- Normal Mode — default.
- Challenge Mode — selectable, with full gameplay differences arriving in Version 3.

Players may switch difficulty through Options during normal gameplay.

Initially, both settings may use Normal Mode trainer data until Challenge Mode is implemented.

Reserve suitable saved settings and plan future save-format changes early.

Additional improvements:

- Expand Pokégear phone capacity so all available trainer contacts can be retained.
- Preserve the ability to remove unwanted contacts.
- Improve swarm notifications with visible on-screen alerts.
- Add Pocket PC access.
- Simplify clock reset.
- Remove artificial saving delays.
- Add a fourth Pokémon stats page.
- Add a third Trainer Card page for Kanto badges.
- Improve Gym Leader portraits on the Trainer Card.
- Add a small clock to the menu.
- Review the default player and rival names.

---

## Version 2 — Items, Poké Balls, tutors, and additional events

**Status: Planned**

Focus on improving convenience, item availability, and optional activities.

### Poké Ball improvements

- Correct documented Apricorn Ball bugs.
- Ensure all original Poké Balls behave correctly.
- Make Kurt finish Apricorn Balls instantly.
- Allow multiple Apricorns to be harvested from trees.
- Consider adding later-generation Poké Balls where feasible.

### Move tutors

Introduce thematic move tutors throughout Johto and Kanto.

Possible locations include:

- Sprout Tower.
- Dark Cave.
- Burned Tower.
- Ice Path.
- Dragon's Den.
- Saffron Fighting Dojo.

Introduce a Hidden Power tutor or move-type changer.

Add portable Move Reminder and Move Deleter functionality where feasible.

### Items and shops

- Improve access to rare held items.
- Introduce a Pokémon League merchant for useful battle items.
- Expand shop inventory capacity.
- Add convenient methods of obtaining PP Ups.
- Improve access to evolution stones and held items.
- Consider a reusable Escape Rope Key Item.

### Other improvements

- Restore the unused Memory Game.
- Change the Lottery Corner to generate a lucky number daily.
- Allow fishing while Surfing.
- Add a Repel renewal prompt.
- Improve Itemfinder usability.
- Add the Mew truck event in Vermilion City.
- Improve selected item and Pokémon gifts.

### Optional Eevee evolution alternatives

Normal Mode may allow:

- Sun Stone → Espeon.
- Moon Stone → Umbreon.

Challenge Mode retains traditional friendship-based evolution.

These rules should be checked when evolution occurs, so changing difficulty does not permanently lock a Pokémon to one method.

Sylveon and its proposed Shiny Stone evolution are deferred until the expanded Pokédex supports Sylveon.

---

## Version 3 — Challenge Mode and trainer improvements

**Status: Planned**

Implement the full Challenge Mode introduced as an Options setting in Version 1.5.

Planned features include:

- Stronger Gym Leader teams.
- Six-Pokémon teams for major Challenge battles where appropriate.
- Improved Elite Four and Champion teams.
- Better trainer AI and held items.
- Modernized movesets and coverage.
- Enhanced rival battles.
- Improved trainer rematches.
- More varied ordinary trainer teams.
- Optional level caps.
- Difficulty-specific badge boost behaviour.
- Set battle style as the Challenge Mode default.
- More strategic Pokémon usage without requiring a full Abilities system.

Review the artificial AI status-move failure chance and other outdated AI restrictions.

Difficulty changes should apply to future battles, not alter battles already underway.

Additional story progression changes, including possible League-access adjustments, require separate design decisions.

---

## Version 4 — Pokémon personality and world interactions

**Status: Planned**

Add dialogue and environmental interactions that give Pokémon and locations more personality.

- Improve interactions with existing overworld Pokémon.
- Add location-specific Pokémon reactions.
- Recognize the player's original starter in selected dialogue.
- Add character reactions from Elm, Oak, Bill, Mom, and others.
- Improve obstacle and field-move dialogue.
- Add small humorous messages and optional Easter eggs.
- Give sacred locations and unusual environments more distinctive interactions.

Keep these additions optional and avoid interfering with core progression.

---

## Version 5 — Restored Kanto maps and legendary encounters

**Status: Planned**

Restore missing Kanto locations using the original Generation I maps as a foundation.

### Viridian Forest

- Restore the forest map.
- Add suitable Bug-type encounters.
- Support tall grass in forest environments.
- Improve trees and Headbutt encounters.
- Add missing Pokémon and alternative starter encounters.

### Safari Zone

- Restore the Safari Zone maps.
- Reintroduce missing Pokémon and exploration content.
- Keep access practical and single-player-friendly.
- Expand Safari-specific mechanics later if appropriate.

### Legendary encounters

Introduce additional Kanto legendary encounters.

A proposed system uses Generation I-inspired monster statues that initiate legendary battles.

Defeated or missed legends may become available again after rechallenging the Elite Four.

Additional content:

- Restore or expand Mewtwo's encounter.
- Restore Vermilion Gym's trashcan puzzle.
- Update the Town Map and relevant navigation.
- Rebalance Pokémon availability as restored locations become accessible.

---

## Version 6 — Expanded Pokédex and additional forms

**Status: Planned; dependent on engine and memory feasibility**

Expand Pokémon support beyond the original 251 species.

Potential additions include:

- Togekiss.
- Mismagius.
- Honchkrow.
- Gliscor.
- Sylveon.
- Other later-generation evolutions of original Pokémon.
- Selected baby Pokémon.
- Alolan, Galarian, Hisuian, and other regional forms.
- Selected Paradox Pokémon, if technically feasible.

Expansion requires changes to species indexing, data tables, sprites, Pokédex handling, and potentially save data.

### Sylveon

In Normal Mode, Sylveon may evolve using a Shiny Stone.

Challenge Mode would retain a friendship-based evolution with a suitable Fairy-related condition.

### Paradox Pokémon

Explore a possible postgame Paradox Disk system that gives eligible original Pokémon alternative evolution paths.

The expanded species and form systems must be stable before these additions are implemented.

Classic Edition retains canonical species typings. Alternative Mega-inspired typings belong to a separate Variant Edition.

---

## Version 7 — Mom's gifts, Eggs, and home improvements

**Status: Planned**

Expand useful rewards and family interactions.

- Introduce a berry or item fridge in the player's home.
- Give Mom additional rewards based on story progress.
- Preserve her optional money-saving function.
- Add badge- and event-based gifts.
- Expand Egg gifts.
- Add baby Pokémon associated with expanded evolutionary families.
- Introduce optional opportunities to obtain remaining starters.
- Add additional decorations through ordinary gameplay.
- Improve Mom's Pokégear tutorial and dialogue.

Rewards should be tied to meaningful progress rather than requiring excessive random calls or repeated interactions.

---

## Version 8 — Modern weather and held-item mechanics

**Status: Planned**

Modernize battle weather without implementing a complete Pokémon Abilities system.

### Snow

Replace Hail with modern Generation IX Snow.

- Add Snowscape as an Ice-type status move.
- Snow increases Ice-type Pokémon's Defense by 50%.
- Blizzard bypasses normal accuracy checks during Snow.
- Snow causes no residual damage.
- Snowscape normally creates five turns of Snow.
- Icy Rock extends Snow created by its holder's move to eight turns.

### Sandstorm

- Increase Rock-type Pokémon's Special Defense by 50% during Sandstorm.
- Modernize Sandstorm duration and interactions.
- Consider a species-specific Sandstorm effect for Tyranitar.

### Sun and rain

- Modernize weather interactions.
- Introduce selected species-triggered weather effects.
- Add Heat Rock and Damp Rock, where appropriate.

### Automatic location weather

Selected battle locations may start with appropriate weather.

Proposed examples:

- Lake of Rage — Rain.
- Cinnabar Island area — Harsh Sunlight.
- Ice Path — Snow.
- Mt. Silver — Snow in suitable areas.

Weather-changing moves should normally be able to override map-started weather.

### Weather items and interface

- Icy Rock.
- Smooth Rock.
- Heat Rock.
- Damp Rock.
- Weather indicators in battle.
- Current time-of-day indicator in battle.

Unused item slots from retired systems may be considered for new held items, subject to save and item-data compatibility.

### Pryce's Snow strategy

Update Pryce's team to use Snow strategically.

Before this release, a suitable Pokémon may hold NeverMeltIce.

After weather modernization, a Snow-setting Pokémon could use Snowscape and hold Icy Rock.

Challenge Mode may use a more advanced weather-based team.

---

# Future editions

After Classic Edition's main roadmap is complete, additional editions may be developed using the finished codebase.

## Variant Edition

A separate edition featuring alternative typings inspired by regional forms and Mega Evolutions.

Possible examples:

- Meganium — Grass/Fairy.
- Typhlosion — Fire/Ghost.
- Feraligatr — Water/Dragon.
- Red Gyarados — Water/Dark.
- Ampharos — Electric/Dragon.
- Special Charizard — Fire/Dragon.

Additional legendary variants and alternate evolution methods may be explored.

These changes do not replace the canonical typings in Classic Edition.

## Larvitar Edition

A separate edition where Larvitar replaces the traditional Johto starter choice.

Potential changes:

- Begin with a Level 5 Larvitar.
- Adjust starter-related dialogue.
- Adapt the rival's team.
- Redistribute the original Johto starters through gifts or Eggs.
- Retain the completed Classic Edition's core mechanics and content.

Both editions remain outside the immediate Classic development schedule.

---

## Upstream base

This project is based on the pret Pokémon Crystal disassembly.

The original upstream project builds the following ROMs:

- Pokemon - Crystal Version (UE) (V1.0) [C][!].gbc `sha1: f4cd194bdee0d04ca4eac29e09b8e4e9d818c133`
- Pokemon - Crystal Version (UE) (V1.1) [C][!].gbc `sha1: f2f52230b536214ef7c9924f483392993e226cfb`
- Pokemon - Crystal Version (A) [C][!].gbc `sha1: a0fc810f1d4e124434f7be2c989ab5b5892ddf36`
- CRYSTAL_ps3_010328d.bin `sha1: c60d57a24bbe8ecf7cba54ab3f90669f97bd330d`
- CRYSTAL_ps3_us_revise_010710d.bin `sha1: 391ae86b1d5a26db712ffe6c28b1867df330d`
- CGBBYTE1.784.patch `sha1: a25517f60ca0e887d39ec698aa56a0040532a4b3`

To set up the repository, see [INSTALL.md](INSTALL.md).

## Credits and references

This project depends on the work of the [pret][pret] community and the [pret/pokecrystal][upstream] disassembly.

Useful upstream resources:

- [**FAQ**](FAQ.md)
- [**Documentation**][docs]
- [**Wiki**][wiki] (includes [tutorials][tutorials])
- [**Symbols**][symbols]
- [**Tools**][tools]
- [Discord (pret, #pokecrystal)](https://discord.gg/d5dubZ3)
- [pret.github.io][pret]

## Disclaimer

Pokémon Crystal Complete is an unofficial fan-made project.

Pokémon and associated trademarks belong to Nintendo, Game Freak, and The Pokémon Company.

This project is not affiliated with or endorsed by these companies.

No copyrighted ROM files are included or distributed in this repository.

[pret]: https://pret.github.io/
[upstream]: https://github.com/pret/pokecrystal
[docs]: https://pret.github.io/pokecrystal/
[wiki]: https://github.com/pret/pokecrystal/wiki
[tutorials]: https://github.com/pret/pokecrystal/wiki/Tutorials
[symbols]: https://github.com/pret/pokecrystal/tree/symbols
[tools]: https://github.com/pret/gb-asm-tools
