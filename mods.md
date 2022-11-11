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


## Extra configuration
### `game.json`
Advanced users can tweak additional options and make minor modifications by changing the values in their [game.json](https://raw.githubusercontent.com/ja2-stracciatella/ja2-stracciatella/master/assets/externalized/game.json). It's installed alongside the rest of the data and
the launcher will show you the location where you can find it. You can make a copy and put it near your `ja2.json` configuration
file, by creating a `data` folder for it. This way you won't lose your settings when you reinstall the engine.

### Other externalized settings
The project extracted many hardcoded values from the original sources into editable text files stored in the [assets/externalized](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/assets/externalized) directory. You can edit weapons, ammo, shops, enemy weapon
choices and much more — **at your own peril**! You can copy them to your user directory the same way as `game.json`.

If you're using the AppImage version and want to modify any of the json files, create `~/.ja2/data` and copy them inside. They
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
  - **Azazel's custom map pack**: See [forum thread](http://thepit.ja-galaxy-forum.com/index.php?t=msg&th=24842&prevloaded=1&&start=40). Contact via forum or Discord (az75) for latest version

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
