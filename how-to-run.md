---
layout: page
permalink: /how-to-run/
---

- [How to Run](#how-to-run)
  * [With the optional launcher](#with-the-optional-launcher)
  * [Without the optional launcher](#without-the-optional-launcher)
- [Extra configuration and modding](#extra-configuration-and-modding)
- [Extra Hotkeys](#extra-hotkeys)

# How to Run

1. Install the **original Jagged Alliance 2 game** on your computer. Make sure you do a full install. Data files from the original game will be used by JA2 Stracciatella. 

2. [Download JA2-Stracciatella](/download) or [compile](https://github.com/ja2-stracciatella/ja2-stracciatella/blob/master/COMPILATION.md) it from the source codes. Install it wherever you want.

##  With the optional launcher

3. Start the launcher and use it to configure the game. It will automatically create the configuration file.

4. Set “JA2 Data Directory” (“JA *Game* Directory” in nightly builds) to point to the directory where the original game was installed during step 1. You can manually enter the directory or use the “...” button to browse your computer. You have to select the directory that **contains** the directory called “Data”. Do not select the “Data” directory.

5. If you haven't installed the English version of the original game, you have to select the correct “Game Version” i.e. localization. Note that the game supports two different Russian localizations: RUSSIAN for the “BUKA Agonia Vlasty” release and RUSSIAN_GOLD for the “Gold” release.

## Without the optional launcher

3. Start the game the first time.  It will create the configuration file in

   - `%USERPROFILE%\Documents\JA2\ja2.json` on Windows.
   - `~/.ja2/ja2.json` on Linux, BSD or OS X.

4. Edit the configuration file and set parameter `game_dir` to point on the directory where the original game was installed on step 1.  You have to use the path to the directory that **contains** the directory called “Data”. Do not use the path to the “Data” directory. For example:

   - `D:\games\ja2\` on Windows.
   - `/home/user/games/ja2-installed` on Linux, BSD or OS X.

5. If you have a non-english version of the original game, you need to start JA2-Stracciatella with parameter telling which version of the game you are using.  For example

   - `ja2.exe -resversion FRENCH` on Windows.
   - `ja2 -resversion FRENCH` on Linux, BSD or OS X.

   You should see the start screen now.

   ![Ja2 Stracciatella start screen](/img/start-screen.png)

Further command line options are available. To list available options run

- `ja2.exe -help` on Windows.
- `ja2 -help` on Linux, BSD or OS X.

## Extra configuration and modding
Advanced users can tweak additional options and make minor modifications by changing the values in their [game.json](https://raw.githubusercontent.com/ja2-stracciatella/ja2-stracciatella/master/assets/externalized/game.json). It's installed alongside the rest of the data and
the launcher will show you the location where you can find it. You can make a copy and put it near your ja2.json configuration
file, by creating a `data` folder for it. This way you won't lose your settings when you reinstall the engine.

The project extracted many other hardcoded values from the original sources into editable text files stored in the [assets/externalized](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/assets/externalized) directory. You can edit weapons, ammo, shops, enemy weapon
choices and much more — **at your own peril**! You can copy them to your user directory the same way as `game.json`. This
also applies to installing 3rd-party mods.

If you're using the AppImage version and want to modify any of the json files, create `~/.ja2/data` and copy them inside. They 
will have precedence over the files supplied by us.

To use one of the [bundled or external mods](features.md#bundled-optional-mini-mods), enable them in the launcher or pass
the following flag when running JA2S:
```
-mod MOD_NAME    Start one of the game modifications. MOD_NAME is the
                 name of modification, e.g. 'from-russia-with-love. See
                 assets/mods folder for possible options'.
```

# Extra Hotkeys

Besides the hotkeys present in the original game, JA2S adds the following for greater ease of use:
- scroll lock: toggle mouse grab in windowed mode
- alt-r: reload held weapon
- ctrl-shift-r: reload weapons of the whole group
- ctrl-l: load game during enemy/militia turn
- ctrl-n: switch between day and night head gear (goggles) for the whole squad
- ctrl-q: swap hand items 
- shift-j: climb through open window
- f: display chance to hit percentages for given tile

These require you toggle a game.json switch:
- d: switch to turnbased mode from realtime

Additionally you can use the middle mouse button to make a merc look into the direction of the cursor.
