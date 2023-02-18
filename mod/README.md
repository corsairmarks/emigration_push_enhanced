# Overview

The Stellaris immigration/emigration system (not automatic Pop resettlement) still exists and works well to redistribute population growth from planets experiencing emigration push to those with immigration pull.  However there aren't many sources of emigration push unless a planet is completely, intentionally mismanaged.  This mod intends to change that with a more aggressive emigration push based on the percentage of used planetary capacity, crime rate, and missing amenities.

Suggested by [Omicron](https://steamcommunity.com/profiles/76561198024964069).

# Changes

Adds a new planetary deposit to each colony five years after its founding, or sooner if the colony has ten or more Pops on the anniversary of its founding. This "Dynamic Emigration Push" deposit exists to boost emigration push from that colony based on a variety of factors. Each percentage point of crime increases emigration push by 1, and missing (negative) amenity increases emigration push by the same amount. Finally, the percentage of Planetary Capacity (mouseover planet size to see Planetary Capacity in a tooltip) that is being used heavily influences emigration push. The formula is `((Pops ÷ Capacity) × 10)² × 0.8` which ultimately is a parabolic function.

## Compatibility

All functionality is implemented by custom script - no Stellaris files are replaced and no script is overwritten. This mod should generally not conflict with other mod.  This mod has built-in compatibility with [Planetary Diversity](https://steamcommunity.com/sharedfiles/filedetails/?id=819148835).

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements.

### When to Install

This mod can be added before or during a game. The new colony emigration deposits are added to each colony on the anniversary of its foundation. It is not recommended to remove this mod during a game; however, Stellaris usually handles missing deposits by removing them and continuing without problems. Always back up your savegame before trying to remove a mod, even this one.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it is experimental.  It is otherwise fully compatible.

### Recommended Companion Mods

* [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) is a large collection my other enhancements for Stellaris; as the name suggests, most are improvements or additions to the basic Stellaris experience
* [More Standard Districts](https://steamcommunity.com/sharedfiles/filedetails/?id=2650611194) gives you more district types to employ your migrating Pops

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/emigration_push_enhanced)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.