# Pokémon Crystal [![Build Status][ci-badge]][ci]

This is an experimental personal project based on [the disassembly of Pokémon Crystal](https://www.github.com/pret/pokecrystal/).
It is meant to serve as a base for an hypothetical further modification of the game. It includes implementing new music and fixing known glitches. While the definitive modification's goals are yet to be determined, it's scope will include maps with their corresponding event data, additional battles and other aspects bound to break savefile compatibility if goals require it. Instead, this repository's changes are expected to retain compatibility with the official builds of the game and thus savefiles.

## Features as of July 20, 2024:
- Music for Cerulean City, Cinnabar Island and Route 24 ported from HGSS.
- Extended the Kanto Trainer Battle theme based on both the HGSS and RGBY versions, also featuring a minor audio bugfix (fun fact: said bug was identified in pokecrystal for the first time while doing this).
- Devamped the characteristic fanfare when player obtains a berry (apricorns trigger the regular fanfare instead). It didn't exist until Generation III.
- Burn, poison and paralysis status effects are taken into account for the final catch rate calculation. Employs [the fix proposed by the pret team](/docs/bugs_and_glitches.md).
- Fixed apriballs based on [the fixes proposed by the pret team](/docs/bugs_and_glitches.md).
- Optimized the forest tree animation during Celebi's event at Ilex Forest, as per [the refactor proposed by the pret team](/docs/design_flaws.md#getforesttreeframe-works-but-its-still-bad).

## To-dos
- Devamp and implement the battle themes for Lugia and Ho-Oh from HGSS.
- Extend the Kanto Gym Leader battle music based on HGSS and Mt. Moon based on HGSS (itself based on RGBY).
- Fix Lake of Rage Magikarp size glitch.
- Consider forcing Gyarados encounters on Lake of Rage prior to the player solving the story scenario that implies this is happening (it doesn't actually happen in-game in base pokecrystal).
- Set up branch to code and test a routine to handle guaranteed 3DV encounters, mirroring guaranteed 3IV encounters from later generations (no actual scenario to implement this in base pokecrystal). These will also double as shiny-locked encounters by design due to how shininess is handled in GB era games.
- Fix other glitches.
- Optimize more areas of code.
- Consider deleting any unused data that doesn't break code/lists/calls, savefiles or the binary itself.

To set up the repository, see [INSTALL.md](INSTALL.md).


## See also

- [**FAQ**](FAQ.md)
- [**Documentation**][docs]
- [**Wiki**][wiki] (includes [tutorials][tutorials])
- [**Symbols**][symbols]

You can Pret on [Discord (pret, #pokecrystal)](https://discord.gg/d5dubZ3).

For other pret projects, see [pret.github.io](https://pret.github.io/).

[docs]: https://pret.github.io/pokecrystal/
[wiki]: https://github.com/pret/pokecrystal/wiki
[tutorials]: https://github.com/pret/pokecrystal/wiki/Tutorials
[symbols]: https://github.com/pret/pokecrystal/tree/symbols
[ci]: https://github.com/pret/pokecrystal/actions
[ci-badge]: https://github.com/pret/pokecrystal/actions/workflows/main.yml/badge.svg
