# Pokémon Crystal Complete

**Pokémon Crystal Complete** is an in-progress, single-player-friendly ROM hack based on the [pret/pokecrystal][upstream] disassembly of Pokémon Crystal.

The goal is to keep the feel of Pokémon Crystal while making the game more complete, more convenient, and more self-contained: every Generation 1 and Generation 2 Pokémon should be obtainable in one save file, version exclusives should be available naturally, trade evolutions should have in-game solutions, cut content should be restored where appropriate, and the level curve / quality-of-life experience should be improved.

This project is currently in planning and early development. The roadmap below describes intended changes, not necessarily completed features.

## Project goals

- Make all Gen 1 and Gen 2 Pokémon obtainable in-game.
- Remove version-exclusive restrictions.
- Make trade evolutions solvable without external trading.
- Restore notable cut or event content, including the GS Ball Celebi event.
- Add selected quality-of-life improvements while preserving the spirit of Crystal.
- Improve the level curve and make team-building feel fairer throughout Johto and Kanto.
- Keep the game single-player friendly while still feeling like Pokémon Crystal.

## Test team

The main regression test team for this project is:

- Steelix
- Typhlosion
- Poliwrath
- Wigglytuff
- Crobat
- Exeggutor

These Pokémon help test evolution methods, friendship, item evolutions, field utility, type changes, battle mechanics, and level-curve changes.

## Planned roadmap

### Milestone 0 — Repo setup / base sync

- Sync with upstream `pret/pokecrystal`.
- Confirm clean build.
- Add releases only when feature chunks are complete and tested.
- Keep `v1.0` reserved for “complete dex + planned core features done.”

### Milestone 1 — Complete dex foundation

This is the heart of the hack and the basis for early testing.

- Remove version exclusivity.
- Make all Gen 1 and Gen 2 Pokémon obtainable (except starters and legendaries).
- Rework wild encounters so late-locked Johto Pokémon have appropriate Johto placements.
- Update the existing in-game Onix trade so the received Onix holds a Metal Coat.
  - This lets Steelix be tested through the original Crystal trade-evolution behavior.
  - The broader item-only evolution system will come later.
- Add Horsea to Good Rod encounters so Kingdra can be obtained and tested before Clair.
- Ensure Celebi and Mew are in the Pokédex and ready to be added later.
- Add Gen 6 experience system / Exp. Share rework.
- Add experience gain from catching Pokémon.
- Add Fairy type.

### Milestone 2 — Evolution and trade fixes

This should come early because it affects dex completion.

- Add a Blackthorn City evolution shop near the Move Deleter / Move Relearner.
- Unlock the shop immediately when Blackthorn City is reached.
- Make rare evolution items usable directly, similar to evolution stones.
- Sell all evolution stones and rare evolution items:
  - Fire Stone
  - Water Stone
  - Thunderstone
  - Leaf Stone
  - Moon Stone
  - Sun Stone
  - King’s Rock
  - Metal Coat
  - Dragon Scale
  - Upgrade
  - Link Cable
- Remove trade requirements from item-based trade evolutions.
- Add Link Cable item support for classic trade evolutions:
  - Kadabra → Alakazam
  - Machoke → Machamp
  - Graveler → Golem
  - Haunter → Gengar
- Add item-only evolution methods:
  - Poliwhirl + King’s Rock → Politoed
  - Slowpoke + King’s Rock → Slowking
  - Scyther + Metal Coat → Scizor
  - Onix + Metal Coat → Steelix
  - Seadra + Dragon Scale → Kingdra
  - Porygon + Upgrade → Porygon2
- Keep Eevee’s original friendship evolutions and add stone-based alternate methods:
  - High friendship during day → Espeon
  - High friendship at night → Umbreon
  - Sun Stone during day → Espeon
  - Moon Stone at night → Umbreon

#### In-game trade fixes

- Onix received holds Metal Coat.
- Olivine Voltorb: replace entirely, maybe with a Pokémon the rival has.
- Pewter Xatu: probably replace, especially if Natu/Xatu are made wild.
- Power Plant Magneton: replace with a Pokémon neither the player nor rival has. Maybe move the Magneton trade concept to Ecruteak City.
- Route 14 Aerodactyl: replace if Aerodactyl becomes wild or fossil-accessible elsewhere.
- Consider two trades for the Johto starters not chosen.

### Milestone 3 — Modern QoL

These are player-facing wins and mostly safe if done carefully.

- Infinitely reusable TMs.
- Show move names for TMs/HMs when receiving or buying.
- Running Shoes.
- Allow field moves if the Pokémon can learn the move.
- Add Pocket PC.
- Don’t lose HP from poison in the overworld.
- Kurt finishes Apricorn Balls instantly.
- Harvest multiple items from fruit trees.
- Daily Lottery instead of weekly.
- Mom’s house fridge gives berries.
- Replace Menu Account with a small clock.
- Move Relearner beside Move Deleter in Blackthorn City.
- Add NPCs that give items / Pokémon where useful.

### Milestone 4 — Battle/mechanics updates

These need heavier testing because they touch balance.

- Add Fairy moves.
- Add Hail.
- Automatic battle weather on certain maps.
- Sandstorm boosts Rock-type Special Defense by 50%.
- Evolution moves.
- Update thaw chances and sleep turns to Gen 7 style.
- Prevent Steel types from being poisoned by Twineedle.
- Grass-type immunity to Powder/Spore-based moves.
- SWSH Friendship Endure.

### Milestone 5 — Maps and restored content

- Restore GS Ball Celebi Event.
- Restore Unused Memory Game.
- Add Viridian Forest map.
- Add Safari Zone map/content.
- Add truck in Kanto with Mew under the truck as a Poké Ball event.
- Add Mewtwo to map
- Make Headbutt work with Kanto trees.
- Restore the trashcan puzzle in Vermilion Gym.
- Add third Trainer Card page for Kanto badges.
- Put Kanto starters in wild locations inspired by Pokémon: Let’s Go, Pikachu! and Pokémon: Let’s Go, Eevee.

### Milestone 6 — Encounter and economy polish

- Rebalance fishing rods or add a new fishing rod.
- Improve swarm system.
- Rock Smash can contain items.
- Improve level curve.
- Final polish pass on encounter rarity, location flavor, and version-exclusive replacements.
- Add Lucky Egg and Shiny Charm, including acquisition events.
- Add Mom menu option: heal Pokémon or receive one daily message.
- Fix Mom’s Pokégear tutorial dialogue so she does not explain it after the player says they already know how to use it.
- Make stationary legends resettable by beating the Elite Four if missed or KO’d.
- Improve shiny odds for wild/static encounters while making Red Gyarados DVs less fixed.

### Milestone 7 — Optional / post-v1

These ideas are currently outside the critical path for v1.

- Regional forms.
- Later-gen evolutions, such as Togekiss, Sylveon, Gliscor, etc.
- More advanced trainer parties with DVs, stat EXP, nicknames, and variable teams.
- Broader new move/type expansion beyond Fairy basics.

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

This is a fan-made project. No ROM files are included or distributed in this repository.

[pret]: https://pret.github.io/
[upstream]: https://github.com/pret/pokecrystal
[docs]: https://pret.github.io/pokecrystal/
[wiki]: https://github.com/pret/pokecrystal/wiki
[tutorials]: https://github.com/pret/pokecrystal/wiki/Tutorials
[symbols]: https://github.com/pret/pokecrystal/tree/symbols
[tools]: https://github.com/pret/gb-asm-tools