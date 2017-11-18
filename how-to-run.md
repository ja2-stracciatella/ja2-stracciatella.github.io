---
layout: page
---

# How to Run

1. Install original Jagged Alliance 2 game on your computer.  Data files from the original game will be used by JA2-Stracciatella. If you're installing the linux port, make sure to copy over files from CD2 too.

1. [Download JA2-Stracciatella](/download) or [compile](https://github.com/ja2-stracciatella/ja2-stracciatella/blob/master/COMPILATION.md) it from the source codes.

1. Start the game the first time.  It will create the configuration file in

   - `%USERPROFILE%\Documents\JA2\ja2.ini` on Windows.
   - `~/.ja2/ja2.ini` on Linux or OS X.

1. Edit the configuration file and set parameter data_dir to point on the directory where the original game was installed on step 1.  For example:

   - `D:\games\ja2\` on Windows.
   - `/home/user/games/ja2-installed` on Linux or OS X.


1. If you have a non-english version of the original game, you need to start JA2-Stracciatella with parameter telling which version of the game you are using.  For example

   - ```ja2.exe -resversion FRENCH``` on Windows.
   - ```ja2 -resversion FRENCH``` on Linux or OS X.

   You should see the start screen now.

   ![Ja2 Stracciatella start screen](/img/start-screen.png)

Further command line options are available. To list available options run

- `ja2.exe -help` on Windows.
- `ja2 -help` on Linux or OS X.

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
