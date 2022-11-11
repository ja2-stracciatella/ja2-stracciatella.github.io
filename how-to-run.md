---
layout: page
permalink: /how-to-run/
---

- [How to Run](#how-to-run)
  * [With the optional launcher](#with-the-optional-launcher)
  * [Without the optional launcher](#without-the-optional-launcher)


# How to Run

1. Install the **original Jagged Alliance 2 game** on your computer. Make sure you do a full install. If you have a game with the 1.13 mod installed, it will not work.

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

**For even more configuration options check the [modding](mods.md) page.**
