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
- Introducing Kanto starters in wild locations inspired by **Pokémon: Let's Go, Pikachu!** and **Let's Go, Eevee!**.
- Relocating Pokémon associated with inaccessible original Kanto areas until those maps are restored.
- Restoring special encounters and legendary events over subsequent versions.

After the Milestone 6 encounter audit, Milestone 7 will document each Pokémon's location, encounter method, time restrictions and version availability. This documentation will not claim unobtainable species are present in Version 1.

## Development and testing

Changes are developed and tested in manageable chunks.

- Keep releases separate from development milestones.
- Test new features before marking them complete.
- Use fresh-save playthroughs for major gameplay and save-structure changes.
- Track bugs, implementation work, and regression tests through GitHub Issues.
- Avoid distributing copyrighted game ROMs; distribute patches and project source code instead.
- Keep the README updated as implementation progresses.

### Current implementation status

The following foundations are committed to the repository, although not all have finished full-playthrough verification:

- Initial upstream synchronization and successful local build.
- Fairy-type groundwork, selected move data and Pokémon typings, including Normal/Fairy Wigglytuff.
- EXP Share reworked into a toggleable Key Item, with catching EXP implemented.
- Horsea added to Good Rod fishing groups and Remoraid encounter groups improved.
- Bug-Catching Contest updated with more Generation II Pokémon.
- Selected Johto/Kanto grass and Headbutt encounters updated.
- Rocky's in-game Onix trade updated to hold Metal Coat, with an item-use evolution fix **implemented, tested, and closed** (Issue #3).
- Dragon Scale changed to support direct Seadra → Kingdra evolution; broader acquisition and regression tests remain outstanding.
- Goldenrod Radio Tower lottery second prize changed from EXP Share to Lucky Egg, pending a further planned reward shuffle.
- Existing Mew and Celebi Pokédex data checked and the data-verification issue **closed** (Issue #8); their actual encounters are future work.

**Current testing:** Milestone 1 fresh-save regression is in progress (Issue #9), with playthrough progress through Goldenrod City. The revised Bug-Catching Contest has been verified in gameplay (Issue #2), and several Fairy-type checks are complete (Issue #7). Further Johto/Kanto progression and full-playthrough checks remain open. See the [Milestone 1 test issue](https://github.com/jennifert/pokecrystal/issues/9) and associated feature issues.

Implemented code, tested behaviour, and future intentions are tracked separately. A closed issue does not imply that every related feature has been fully expanded or released.

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

**---**

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

This milestone verifies the initial encounter, Fairy-type, evolution groundwork, and experience-system changes.

#### Encounter changes

- Remove selected version-exclusive restrictions.
- Improve Johto Pokémon availability, including earlier Houndour, Murkrow, Mareep, and selected other species.
- Add Horsea to Good Rod encounters; improve Remoraid fishing groups.
- Update selected Bug-Catching Contest encounters to use Generation II Pokémon.
- Expand selected Headbutt encounters and add some missing Kanto species to existing locations.

#### Mechanics

- Add Fairy-type groundwork, modern typings for selected Pokémon, and relevant type/move interactions.
- Rework EXP Share into a toggleable Key Item.
- Award EXP for successful captures, but not for failed catches.
- Support Rocky's Metal Coat evolution by item use; Issue #3 is fixed and closed.
- Verify the existing Mew/Celebi Pokédex records; Issue #8 is closed (encounters are separate future work).

#### Testing

- [x] Confirm the local build and start a fresh-save playthrough.
- [x] Test progression from New Bark Town through Violet City.
- [x] Test and close Rocky's Metal Coat evolution issue (#3).
- [x] Verify Mew/Celebi Pokédex data (#8).
- [ ] Continue the full Johto and Kanto playthrough, including Red (#9).
- [x] Verify all 11 regular revised Bug-Catching Contest species appear and the contest ends normally (#2).
- [ ] Verify remaining revised wild encounters, Headbutt and fishing groups (#2, #4).
- [ ] Test EXP Share distribution/toggle and catching EXP in all relevant cases (#5, #6).
- [ ] Confirm EXP awarded after a successful capture can correctly trigger level-ups and move-learning prompts (#6).
- [x] Verify Poison and Steel are super effective against Fairy, and Fairy resists Fighting, Bug and Dark (#7).
- [ ] Finish other Fairy-type checks: Pokémon types, evolution typing, Dragon immunity, and Fairy typing of Charm, Sweet Kiss and Moonlight (#7).
- [ ] Retest saving, loading, story events and other regression cases.

**Bug-Catching Contest playtest (24 November 2026):** 96 recorded encounters across all 11 regular species: Ledyba 30, Spinarak 17, Venonat 13, Pineco 7, Beedrill 6, Heracross 6, Butterfree 5, Paras 5, Pinsir 3, Scyther 3 and Yanma 1. The contest ended correctly when Park Balls ran out; the player placed second. These are *observed encounter counts*, not the programmed encounter probabilities. Contest availability is verified; encounter-rate balancing remains for Milestone 6.

Track current results in [Milestone 1 GitHub Issues](https://github.com/jennifert/pokecrystal/issues?q=is%3Aopen%20milestone%3A%22Milestone%201%22). Later quality-of-life and balance observations are recorded for their scheduled milestones rather than treated as Milestone 1 blockers.

### Milestone 2 — Evolution and trade fixes

**Status: Planned; Rocky/Metal Coat tested, Dragon Scale code committed and other evolutions pending**

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

Rocky's Metal Coat item-use evolution has already been implemented and tested. Dragon Scale item-use support is also in code, but Kingdra acquisition and other evolution cases still need gameplay testing.

Horsea evolves into Seadra at Level 32; Dragon Scale should then evolve Seadra directly into Kingdra without trading.

Dragon Scale must be obtainable before challenging Clair.

#### Evolution-item merchant

Add an evolution-item shop in Blackthorn City, accessible immediately upon reaching the city. **Keep Blackthorn's Move Deleter available during Milestone 2** and repurpose that NPC only after Milestone 3 implements and tests ordinary HM move forgetting/replacement.

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
- Allow compatible Pokémon to perform field moves without occupying move slots, while retaining badge/story progression restrictions.
- Add Running Shoes.
- Add a **free Move Reminder through Pokémon PCs**, not a separate NPC. Include eligible Level 1/evolution-only moves; allow ordinary move replacement and HM deletion once tested.
- Retire or repurpose Blackthorn's Move Deleter only when Pokémon can forget/replace HM moves without that NPC.
- Remove overworld poison damage.
- Avoid unnecessary EXP calculations for Level 100 Pokémon.
- Improve access to essential evolution and training items.

#### Early Flash, Fly and Mud-Slap progression

**Planned for Milestone 3; not available in the current build.** Separate early *field travel* from later *battle move use* to avoid overpowering the first Gyms.

- **Sprout Tower Elder Li:** retain HM05 Flash; defeating him unlocks Flash outside battle without a Gym badge.
- **Falkner:** award HM02 Fly instead of TM31 Mud-Slap; the Zephyr Badge permits field Fly to previously visited destinations (no Storm Badge required), using eligible Pokémon.
- **Violet City Mart:** sell TM31 Mud-Slap.
- **Before Jasmine's Lighthouse medicine request:** Fly works for field travel only and cannot be taught as a battle move, avoiding unusable battle moveslots.
- **Jasmine requests medicine for Amphy:** unlock teaching and using Fly in battle through existing `EVENT_JASMINE_EXPLAINED_AMPHYS_SICKNESS`, before Chuck's Gym.
- Update Falkner, Elder Li and Chuck's wife's dialogue; test eligible Pokémon, Fly-point and story restrictions, event flags, saving/loading and full-Bag gifts. Chuck's wife's replacement gift is planned for Version 1.5.

#### Early-game rewards and item redistribution

Rearrange existing gift rewards without changing the basic early-game story:

- **Show Togepi/Togetic to Professor Elm:** receive the toggleable **EXP Share Key Item** instead of Everstone.
- **Mom, after Falkner:** receive a one-time **Everstone** gift, gated by the Zephyr Badge/defeating Falkner.
- **Elm's aide/scientist:** retain his original gift of **five Poké Balls**.
- **Mr. Pokémon's Red Scale exchange:** receive **Lucky Egg** instead of EXP Share.
- **Goldenrod Radio Tower lottery, second prize:** replace the current Lucky Egg reward with **Scope Lens**.
- Update NPC text, one-time event flags and checks for a full Bag. Verify rewards survive saving/loading and cannot be duplicated unintentionally.

**Important:** These reward changes are *planned*, not implemented in the current playable build. For now, Elm still gives Everstone for Togepi, Mr. Pokémon gives EXP Share for the Red Scale, and the lottery awards Lucky Egg as second prize.

The expanded Bag, Pocket PC, substantial Options changes and saving-system changes are reserved for Version 1.5.

### Milestone 4 — Moves and battle mechanics

**Status: Planned**

Review original moves, learnsets and move-slot use before introducing new moves. Check power, accuracy, PP, typing, level-up timing, Egg Moves, TM/HM compatibility, evolution moves and species-specific coverage.

#### Early learnset improvements

- **Cyndaquil:** learn an early Fire-type attack such as Ember around Level 6, before Smokescreen.
- **Totodile:** learn Water Gun around Level 6–7, before Rage.
- **Chikorita:** receive an earlier Grass-type attack, provisionally Razor Leaf around Level 6; assess balance against the opening Gyms.
- **Togepi:** hatch with a dependable damaging move instead of redundant Growl/Charm support only. Preferred option is to **replace Growl with Disarming Voice** (proposed 40-power Fairy move); **Swift** (60-power Normal move) remains the fallback if the new Fairy move or its balance is not ready. Keep Charm for support and Metronome at Level 7. Propose increasing Metronome from 10 to **20 PP** after balance testing.
- **Zubat:** replace its initial weak Leech Life with Absorb at Level 1, modernize Leech Life to 80 power and move it later in the Zubat/Golbat/Crobat line (around Level 30–35, subject to balance).
- **Jynx:** add Psychic as a **Level 1, Move Reminder-only** option after evolution. Keep Smoochum's current learnset and Level 30 evolution unchanged; this uses the Milestone 3 PC Move Reminder.
- Review Togetic's starting moves and other baby Pokémon that hatch without useful attacks.
- Test newly hatched Pokémon, learnset ordering, existing saves and move-learning prompts.

#### Move-slot and moveset review

- **Spider Web → Sticky Web:** repurpose Spider Web's move slot as a Bug-type entry hazard (proposed 20 PP). Grounded opponents switching in lose one Speed stage; Flying-type Pokémon are unaffected. Rapid Spin should clear webs on the user's side. Retain Mean Look as the trapping move; review original Spinarak/Ariados learners and other appropriate species.
- **Fury Swipes → Facade:** proposed replacement, not yet finalized; update affected learnsets if adopted.
- **Fury Attack:** on the removal/replacement shortlist, with no replacement chosen yet.
- **Fury Cutter:** keep and modernize; do not confuse with Fury Swipes or Fury Attack.
- Consider other modern attacks (such as Scale Shot, Drain Punch, Water Pulse, Magnet Rise, Aerial Ace, Dual Wingbeat, Flip Turn and Volt Switch) as available move slots and engine support permit.
- Modernize weak/outdated existing moves, including Leech Life, while preserving distinctive original moves where useful.
- **Fly:** raise from Crystal's current 70 power to modern **90 power** in Milestone 4, after the Milestone 3 Lighthouse battle-use unlock is working; early travel-only Fly must not provide a powerful attack before Bugsy.

#### Battle mechanics

- Complete and test the modern Fairy-type chart.
- Correct outdated Ghost/Dark vs Steel interactions and Dragon Fang/Dragon Scale type-boost behaviour.
- Modernize sleep and thaw rules; reduce confusion self-hit chance.
- Fix Steel-type poisoning from Twineedle and add appropriate Grass-type powder immunities.
- Review evolution moves and documented Generation II mechanics bugs.

Every new effect needs focused regression tests. Weather modernization remains reserved for Version 8.

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

Improve the original **Normal Mode** experience without using the full Challenge Mode systems planned for Version 3.

#### Trainers and level curve

- Rebalance **all 16 Gym Leaders and every regular trainer inside their Gyms**, alongside ordinary trainers, rivals, Team Rocket and the Elite Four. Improve themed species variety, evolutionary stages, levels and moves, plus item/money rewards.
- Reduce repeated Pidgey, Spearow, Caterpie, Weedle and similar trainer teams; give Bug Catchers more species and appropriate evolved Pokémon (such as Scyther, Pinsir, Heracross and later Scizor).
- Review early-game balance with Chikorita and readily obtainable Rock-, Ground- and Normal-type support Pokémon.
- **Falkner proposal:** raise Pidgey from Level 7 to approximately Level 10 and Pidgeotto from Level 9 to approximately Level 12; retain thematic Flying-type moves, Gust and Mud-Slap as appropriate. This is a balancing proposal, not an implemented change. Moving TM31 to the Mart does not require removing Mud-Slap from Falkner's Pokémon.
- **Whitney, approved Normal Mode team:** **Clefairy Lv17** (Fairy support), **Smeargle Lv18** (Sketch with support/coverage), **Girafarig Lv18** (Normal/Psychic) and **Miltank Lv20** (signature Rollout ace). This replaces the earlier Aipom proposal. Sketch is agreed, but Smeargle's remaining moves are still provisional (Seismic Toss, Thunder Wave and Icy Wind are candidates). Update Goldenrod's Gym trainers too.
- Review trainer levels through Johto/Kanto and improve swarm availability and shiny-related mechanics where appropriate; revisit Red Gyarados's fixed DVs.

#### Full wild-encounter audit

After the initial Milestone 1 availability changes, review **every encounter method** across Johto and Kanto: grass, time-of-day/day-of-week changes, fishing, Surf, Headbutt, Rock Smash, swarms and special encounters. Compare appropriate GSC/HGSS placements, expand variety, reduce repetitive duplicates, and preserve early access to species such as Phanpy while improving places such as Route 46.

#### Fishing progression overhaul

The current fishing file already has targeted changes (notably Good Rod Horsea and revised Remoraid groups), but a full three-rod redesign is **not yet implemented**.

- **Old Rod:** more varied, low-level, generally unevolved fish and aquatic Pokémon rather than overwhelming Magikarp repetition.
- **Good Rod:** a broader pool of stronger unevolved species and suitable middle-stage evolutions.
- **Super Rod:** the widest pool, with rare catches and appropriate evolved Pokémon such as Kingler, Seaking or Tentacruel where they make sense.
- Preserve rare unevolved species on stronger rods when desirable; do not require all Super Rod encounters to be fully evolved.
- Balance levels and encounter rates by habitat, location, time and progression. Preserve **Horsea with the Good Rod before Clair**.
- Test each rod in every relevant fish group, including swarm/time-dependent tables.

**Bug-Catching Contest balancing:** review levels and encounter rates during Milestone 6; 96 observations confirm each regular species is obtainable, not its true encounter probability. Preserve the now-tested normal contest ending.

The complete final Pokémon encounter/location guide will be written **after** this audit, during Milestone 7. Advanced six-Pokémon Gym teams and Challenge Mode AI changes remain scheduled for Version 3.

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
- After Milestone 6, publish a verified species-by-species encounter guide (planned `docs/pokemon-locations.md`) covering location, method, time restrictions and any unavailable species.
- Document other features deferred to later releases.
- Update the README and release notes.

**Version 1 will be considered ready when its included features are stable and tested, not when all future planned Pokémon and content have been added.**

**---**

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

Redistribute former Mystery Gift decorations to ordinary gameplay. Once Fly moves to Falkner, **Chuck's wife** can give a replacement reward after Chuck is defeated. Select it from retired Mystery Gift items/decorations during the Version 1.5 cleanup; the specific gift is not yet decided.

Potential sources:

- Existing NPCs.
- Mahogany Town shop.
- Goldenrod and Celadon merchants.
- Optional gifts and exploration rewards.

### Options menu and save foundations

Introduce a visible difficulty setting:

- **Normal Mode:** default.
- **Challenge Mode:** selectable in Options, with the full difficulty differences arriving in Version 3.

Players may switch difficulty during normal play. Until Version 3, the Challenge setting may temporarily use the Normal trainer data. Plan the save-data and Options architecture with future expansion in mind.

#### Expanded Bag and storage

- Expand item capacity beyond the original small pocket limits; consider separate Item, Medicine, Berry, Apricorn, Ball, Key Item and TM/HM categories.
- Audit the Bag, PC storage, item constants, menus and save structures before changing pocket definitions.
- Add portable Pocket PC access if feasible without undermining existing PCs.
- Keep bag/PC item moves, sorting, item use and save compatibility safe.

#### Saving and New Game safety

- Remove artificial saving pauses and redundant confirmation/overwrite prompts: one clear confirmation to save in normal circumstances.
- When selecting **New Game** while another save exists, present a clear warning before starting; do not erase the old save merely by entering New Game. Replacement should happen only when the new game is actually saved, with appropriate safeguards.
- Test save integrity, old/new trainer IDs, interruptions and overwrite behaviour.

#### Pokégear, swarms and interface

- Expand Pokégear phone capacity so every obtainable trainer number can be stored; retain the ability to delete unwanted contacts.
- Display short on-screen swarm alerts rather than relying only on phone calls; account for swarms that begin without a call.
- Fix Mom's phone tutorial so answering that the player already knows how to use the phone doesn't repeat the full explanation.
- Simplify clock reset and add a small menu clock where practical.
- Add a fourth Pokémon stats page, a third Trainer Card page showing Kanto badges, and improved Gym Leader portraits.
- Review player and rival default names and other legacy dialogue/menus.

#### Traded Pokémon obedience

- Raise the starting outsider/traded Pokémon obedience threshold from the original Level 10 to **Level 15**.
- Explore modern-style behaviour where a Pokémon received within the current obedience limit continues to obey as it levels up, even after evolving; this requires tracking the appropriate received-level data and checking save compatibility.
- Preserve the existing higher badge-based obedience thresholds unless separately revised.
- Keep **traded-Pokémon obedience distinct from Challenge Mode level caps**. Rocky is a useful regression case.

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

Expand convenience around the **Milestone 3 Pokémon PC Move Reminder** if useful. HM forgetting/replacement should work before the Blackthorn Move Deleter is retired; a duplicate Move Reminder NPC is unnecessary.

### Items and shops

- Improve access to rare held items.
- Introduce a Pokémon League merchant for useful battle items.
- Expand shop inventory capacity.
- Add convenient methods of obtaining PP Ups.
- Improve access to evolution stones and held items.
- Add a **reusable Escape Rope Key Item**, granted early enough to help before Union Cave; usable without consumption in locations where Escape Rope would normally work.

### Bug-Catching Contest interface

- Display **remaining Park Balls** and **remaining time (minutes:seconds)** during the contest in a compact, unobtrusive GBC-friendly display or easily accessible status panel.
- Refresh counts when balls are spent and time passes; preserve existing contest mechanics and judging.
- Consider an optional **End Contest** command so players can finish without exhausting their Park Balls.

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

**---**

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
- Optional Challenge Mode level caps (no level cap in Normal Mode). Tentative early ace-level caps: **12 before Falkner, 16 before Bugsy, 20 before Whitney**, subject to balance testing. Check catching EXP, Exp. Share and candy interactions with the cap.
- Difficulty-specific badge boost behaviour.
- Set battle style as the Challenge Mode default.
- More strategic Pokémon usage without requiring a full Abilities system.

Review the artificial AI status-move failure chance and other outdated AI restrictions.

Difficulty changes should apply to future battles, not alter battles already underway. Level caps apply to the entire party in Challenge Mode and are **separate** from the Version 1.5 outsider/traded Pokémon obedience thresholds.

Additional story progression changes, including possible League-access adjustments, require separate design decisions.

**---**

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

**---**

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

**---**

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

**---**

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

**---**

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

**---**

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

**---**

## Upstream base

This project is based on the pret Pokémon Crystal disassembly.

The original upstream project builds the following ROMs:

- Pokemon - Crystal Version (UE) (V1.0) [C][!].gbc `sha1: f4cd194bdee0d04ca4eac29e09b8e4e9d818c133`
- Pokemon - Crystal Version (UE) (V1.1) [C][!].gbc `sha1: f2f52230b536214ef7c9924f483392993e226cfb`
- Pokemon - Crystal Version (A) [C][!].gbc `sha1: a0fc810f1d4e124434f7be2c989ab5b5892ddf36`
- CRYSTAL_ps3_010328d.bin `sha1: c60d57a24bbe8ecf7cba54ab3f90669f97bd330d`
- CRYSTAL_ps3_us_revise_010710d.bin `sha1: 391ae86b1d5a26db712ffe6c28bbf2a1f804c3c4`
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
