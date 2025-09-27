---
layout: page
permalink: /mods/
---

- [Extra configuration](#extra-configuration)
  * [game.json](#gamejson)
  * [Other externalized settings](#other-externalized-settings)
- [List of mods](#list-of-mods)
  * [Bundled mini-mods](#bundled-mini-mods)
  * [Other official mods](#other-official-mods)
  * [External mods](#external-mods)
- [Installing mods](#installing-mods)
- [For modders](#for-modders)
  * [Using JSON patches](#using-json-patches)

## Extra configuration
### `game.json`
Advanced users can tweak additional options and make minor modifications by changing the values in their 
[game.json](https://raw.githubusercontent.com/ja2-stracciatella/ja2-stracciatella/master/assets/externalized/game.json).
It's installed alongside the rest of the data and the launcher will show you the location where you can find it. 

You can make a copy and put it near your `ja2.json` configuration file by creating a `data` folder for it.
This way you won't lose your settings when you reinstall the engine. As of v0.22 [creating
a patch](#using-json-patches) for the file **is strongly suggested**, so it's less likely to become stale with later
JA2S releases, meaning you're less likely to miss cool new features or break the game.

### Other externalized settings
The project extracted many hardcoded values from the original sources into editable text files stored in the [assets/externalized](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/assets/externalized) directory in the JSON format. You can edit weapons, ammo, shops, enemy weapon
choices and much more — **at your own peril**! You can copy them to your user directory the same way as `game.json` or
generate more robust patches [as discussed below](#using-json-patches).

Most JSON files come with descriptions of their purpose and fields at the very beginning. Many of them also have namesake validation
[(schema) files](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/rust/stracciatella/src/schemas/yaml), 
which also provide some documentation.

If you're using the AppImage version and want to modify any of the JSON files, create `~/.ja2/data` and copy them inside. They
will have precedence over the files supplied by us.


## List of mods
### Bundled mini-mods
A few data-altering [mods](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/assets/mods) are included with JA2S, but **must be explicitly selected to be used**:
  - **Generous Rebels**, **From Russia With Love**: extra items in Omerta
  - **Honest IMP quiz questions**: the satirical answers now include the personality aspect that they would contribute to
  - **O Fortuna**: dramatic intro music for Jagged Alliance 2

### Other official mods
Several additional mods can be downloaded from our [GitHub organization](https://github.com/ja2-stracciatella). Either individually or conveniently [bundled in a single file](https://github.com/ja2-stracciatella/ja2-stracciatella-modpacks/releases/latest).

Currently the bundle includes:
  - **Stracciatella Gun Pack by Kaerar**
  - **Night Ops map pack for JA2**: Map pack for JA2 Stracciatella, adapted from the Night Ops JA2 mod

Then there is of course the [Wildfire support mod](features.md#wildfire-support).

### External mods
Mods not hosted by us include:
  - **Return to San Amaro** by Azazel and Papill0n: See [forum thread](http://thepit.ja-galaxy-forum.com/index.php?t=msg&th=25074&goto=365180&#msg_365180) for latest downloads.
  - **Azazel's custom map pack**: [Download here](https://storage.rcs-rds.ro/links/4729f8d6-f44b-42b7-aa3e-e0ddc6deead6?path=%2FJA_2%2FStracciatella%2FMods). See [forum thread](http://thepit.ja-galaxy-forum.com/index.php?t=msg&th=24842&prevloaded=1&&start=40) for discussions.
  - **Sweet Revenge** by Inveris: See [forum thread](http://thepit.ja-galaxy-forum.com/index.php?t=msg&th=25259&start=0&) for latest downloads.
  - RogueLike by Ashley Pringle: made obsolete by *Dead is Dead* game mode
  - Alternate IMP creation by mgl: merged into core, enable `pick_skills_directly` in `game.json`

Let us know if you're working on a mod, so we can feature it here!


## Installing mods
Most mods come with their own installation instructions. Some vanilla JA2 mods may require overwriting existing files, a need that JA2S obviates — mod files and folders have priority. So in general it's enough to copy the whole mod folder into a `mods` folder in your JA2S user directory (where you have `ja2.json`). You will have to create this mods folder yourself.

JA2S enables running multiple mods at once, but beware: there are no guarantees mods will work with each other. If two mods modify the same file, only one of the changes will have an effect in game — the one from the mod that was loaded last.


## For modders
For mods to show up in the launcher, a `manifest.json` is required. It currently has 3 mandatory keys: name, description and version. An [example from Night Ops maps](https://github.com/ja2-stracciatella/mod-nightops-maps/blob/master/manifest.json) looks like this:

```
{
    "name": "Night Ops maps",
    "description": "This map pack contains more than 60 town and strategically important sectors from Night Ops mod, adapted to the original balance of Jagged Alliance 2.",
    "version": "0.1.0"
}
```

You can also find some extra tooling in our GitHub organization. See for example the [ja2-open-toolset](https://github.com/ja2-stracciatella/ja2-open-toolset#readme) and the prototype of [straccatella toolset](https://github.com/ja2-stracciatella/stracciatella-toolset#readme) for editing json files.

If you have any questions, reach out to us on the usual channels. There are some labels on our issue tracker that are more likely to be interesting to modders: [modding](https://github.com/ja2-stracciatella/ja2-stracciatella/issues?q=is%3Aopen+is%3Aissue+label%3Amodding), [externalization](https://github.com/ja2-stracciatella/ja2-stracciatella/issues?q=is%3Aopen+is%3Aissue+label%3Aexternalization), [modding-breaking-change](https://github.com/ja2-stracciatella/ja2-stracciatella/issues?q=is%3Aopen+is%3Aissue+label%3Amodding-breaking-change).

### Using JSON patches
As of v0.22 JA2S supports the [JSON Patch](https://datatracker.ietf.org/doc/html/rfc6902/#section-4) format. What that means is that you don't have to maintain copies
of whole JSON files, but just specify what you want to change.
This has several benefits:
- it makes the mod more resilient to changes to the files upstream,
- it makes it possible for several mods to change the same file while maintaining compatibility (provided the changes don't conflict)
- it reduces size and maintenance burden.

Like with the full files themselves, the patches will be applied in the mod loading order, oldest enabled mod to first. So if you want to create a mod for a mod, the user will just have
to make sure your mod is in the list after it. If you're unsure about the order, you can run JA2S and it will log the mod priorities (and paths) on startup.

#### Creating patches
If you want to change `FILE.json`, you will have to create `FILE.patch.json`. The easiest way is to make a copy of the file, change it however you desire,
then use a [patch generator](https://chbrown.github.io/rfc6902/) to create the contents for the patch file. With the linked tool this would mean you paste
the original file in the "input" box, the changed one in the "output" box and then "results" will change to show the patch. You should save it to your
configuration folder: see note in the [game.json](#gamejson) section.

That particular tool unfortunately does not support JSON comments. If you get parsing errors, you can try stripping all lines with `//` from both boxes first,
since it is very likely the patch will apply normally to the original file (with the comments). Or you can write the patch manually, following the examples.
Here's one for `game.json`, turning on multiple interrupts, IMP skill picking instead of the quiz and allowing for less skilled IMPs:
```json
[
  {
    "op": "replace",
    "path": "/multiple_interrupts",
    "value": true
  },
  {
    "op": "replace",
    "path": "/imp/min_attribute_points",
    "value": 15
  },
  {
    "op": "replace",
    "path": "/imp/pick_skills_directly",
    "value": true
  }
]
```
