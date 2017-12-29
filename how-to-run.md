---
layout: page
---

# How to Run

1. Install original Jagged Alliance 2 game on your computer.  Data files from the original game will be used by JA2-Stracciatella. If you're installing the linux port, make sure to copy over files from CD2 too.

2. [Download JA2-Stracciatella](/download) or [compile](https://github.com/ja2-stracciatella/ja2-stracciatella/blob/master/COMPILATION.md) it from the source codes.

##  With the optional launcher

3. Start the launcher and use it to configure the game. It will automatically create the configuration file.

4. Set “JA2 Data Directory” to point to the directory where the original game was installed during step 1. You can manually enter the directory or use the “...” button to browse your computer.

5. If you haven't installed the English version of the original game, you have to select the correct “Game Version” i.e. localization. Note that the game supports two different Russian localizations: RUSSIAN for the “BUKA Agonia Vlasty” release and RUSSIAN_GOLD for the “Gold” release.

## Without the optional launcher

3. Start the game the first time.  It will create the configuration file in

   - `%USERPROFILE%\Documents\JA2\ja2.ini` on Windows.
   - `~/.ja2/ja2.ini` on Linux, BSD or OS X.

4. Edit the configuration file and set parameter data_dir to point on the directory where the original game was installed on step 1.  For example:

   - `D:\games\ja2\` on Windows.
   - `/home/user/games/ja2-installed` on Linux, BSD or OS X.

5. If you have a non-english version of the original game, you need to start JA2-Stracciatella with parameter telling which version of the game you are using.  For example

   - ```ja2.exe -resversion FRENCH``` on Windows.
   - ```ja2 -resversion FRENCH``` on Linux, BSD or OS X.

   You should see the start screen now.

   ![Ja2 Stracciatella start screen](/img/start-screen.png)

Further command line options are available. To list available options run

- `ja2.exe -help` on Windows.
- `ja2 -help` on Linux, BSD or OS X.

# Extra Hotkeys

Besides the hotkeys present in the original game, JA2S adds the following for greater ease of use:
- scroll lock: toggle mouse grab in windowed mode
- alt-r: reload held weapon
- ctrl-l: load game during enemy/militia turn
- ctrl-n: switch between day and night head gear (goggles) for the whole squad
- ctrl-q: swap hand items 
- shift-j: climb through open window

These require you toggle a game.json switch:
- d: switch to turnbased mode from realtime

Additionally you can use the middle mouse button to make a merc look into the direction of the cursor.
