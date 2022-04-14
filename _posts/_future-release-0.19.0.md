---
layout: post
title: Release 0.19.0
---

The Jagged Alliance 2 Stracciatella team is proud to present a new release showcasing a year of work. It includes several new features, plenty of bugfixes compared to previous versions and the original game, clean-ups of the old code base, and most notably a new saving&loading screen. Our Chinese fans will now be able to play the game in their own language (zh_CN).

(stats as of 2022-04-13) Through 275 commits at least 41 bugs were fixed, 15 of which are known to affect vanilla.

__New Features__:
  - (Simplified) Chinese language support
  - Support for arbitrary amounts of saved games which are all displayed in the same list whether with or without mods
  - Modding improvements
    - More hardcoded values and assumptions are now externalized to additional or improved json files for easy editing (item graphics, vehicles, starting sector, squad size, weapon shooting sounds)
    - Mods can provide manifest files with important metadata — to be displayed in the launcher and stored in saved games
  - Configurable website loading time, maximum squad size game speed and an option to refill totally defeated patrol groups (set in `game.json`)
  - The optional chance-to-hit now accounts for aiming and is not tied to F, but `show_hit_chance` in `game.json`
  - Improvements to the android work-in-progress port and support for the Apple M1 chips

**NOTE**: automatic brightness correction has been disabled, so pass eg. `-brightness 1.3` on the command line if you need to increase brightness/gamma to 130%.

We are shipping pre-built packages for Linux, Windows and OS X. This should help users to easily get started with Jagged Alliance 2 Stracciatella. For users willing to take a risk we also provide automatically created [nightly builds](https://storage.googleapis.com/ja2-builds/index.html#nightlies/).

__Download__:
[http://ja2-stracciatella.github.io/download/](http://ja2-stracciatella.github.io/download/)
Make sure to uninstall any previous versions before installing.

__Main Changelog__:

- Bugfix (vanilla): AI Order/Attitude incorrect comparison (#1385)
- Bugfix (vanilla): Fix graphical glitching during scrolling when merc lights are enabled (#1437)
- Bugfix (vanilla): GuiBaseJA2Clock signed/unsigned inconsistency (#1386)
- Bugfix (vanilla): Incorrect adjacent teammates search (#1388)
- Bugfix (vanilla): Incorrect AI function call (#1391)
- Bugfix (vanilla): Incorrect armour type comparison when searching for better items on the ground (#1392)
- Bugfix (vanilla): Incorrect condition, || instead of && (#1463)
- Bugfix (vanilla): Incorrect target level when calculating throw params (#1397)
- Bugfix (vanilla): Smoke on the floor level affects vision on the roof. (#1394)
- Bugfix (vanilla): Throw search ends if one the checked spots was too far (#1384)
- Bugfix (vanilla): When setting special movement cost for fences, check that tile after the fence is not blocked (#1389)
- Bugfix (vanilla): Wrong amount shown on items pop-up (#1336)
- Bugfix (vanilla): Zero calculated CTH can result in 1% actual bullet hit (#1393)
- Bugfix (vanilla): Crash when handing Fatima the letter while another merc discovers an item (#1378)
- Bugfix (vanilla): Fix camera focus when clicking on overhead map (#1438)
- Bugfix (vanilla): Stuck at automatic first aid screen (#1407)
- Bugfix: Artifacts when entering a map (#95)
- Bugfix: Build on mingw64 - Error with copying file stracciatella_c_api.lib (#1296)
- Bugfix: Crash when opening "Continue Saved Game" screen (#1452)
- Bugfix: Error when building on MSYS2 system on windows (#1398)
- Bugfix: Game crash in P3 basement (#1443)
- Bugfix: 'No such file or directory' when attempting to save under some circumstances as of e202b45 (#1379)
- Bugfix: Replying to Mike crashes the game (#1444)
- Bugfix: Allow more than 1 dead mercs on squad (#1410)
- Bugfix: Chat boxes sometimes don't fit the text (#1477)
- Bugfix: Crash when doing aimed burst to certain NPCs (#1365)
- Bugfix: Failed assertion (debug build) or segfault (RelWithDebugInfo) when picking up a delivery, or collecting a bounty with all inventory slots full (#1387)
- Bugfix: Fix chance-to-hit preview for rooftop targets (#1427)
- Bugfix: Fixing signedness errors in Strategic AI (#1420)
- Bugfix: Fix UI overlay glitches in tactical UI (#1424)
- Bugfix: Game temporarily hangs (stopwatch) when spotting an item mid movement (#1367)
- Bugfix: Minor regression of VFS case-insensitivity (#1465)
- Bugfix: Refund the correct amount of medical deposit (#1412)
- Bugfix: Can't save games on Android since JA2S 0.19 20210920 build (#1447)
- Bugfix: Do not adjust screen brightness unless requested (#1383)
- Bugfix: Error saving game (#1472)
- Bugfix: Fix #1379: Read and reset sector flags when removing temp files (#1381)
- Bugfix: Truncated error message when failing to build virtual file system (VFS) (#1433)
- Bugfix: Passing bad command-line flags doesn't show the whole -help (#1494)
- Bugfix: Update fltk library to version 1.3.8 (#1500)
- Bugfix: Remove explicit architecture in macOS toolchain file (#1506)
- Bugfix: Update SDL2 to 2.0.20 for macOS (#1505)
- Editor: Better editor save load dialog (#1362)
- Editor: Slf archive and folder confusion (#667)
- Enhancement: Supporting chinese localization (#810)
- Enhancement: Added option for mouse cursor to always be visible in tactical view (#1372)
- Enhancement: Add OpenBSD toolchain file and update build instructions (#1396)
- Enhancement: Add the possibility to provide a mod manifest (#1432)
- Enhancement: Appending extra game states at the end of Saves (#1282)
- Enhancement: Change the squad save format (#1411)
- Enhancement: Config var for scaling website loading time on laptop (#1376)
- Enhancement: Dynamic tactical bottom bar (#1409)
- Enhancement: Excessive temp file usage in .ja2/tmp/temp (#1255)
- Enhancement: Externalize item graphics (#1459)
- Enhancement: Externalize squad size (#1415)
- Enhancement: Externalize all weapon shooting sounds properly (#1456)
- Enhancement: Externalize vehicles (#1400)
- Enhancement: Externalizing starting sector (#1359)
- Enhancement: Feature Request: Chance-to-hit feature improvements (#1368)
- Enhancement: Highlight compatible items in sector inventory (#1439)
- Enhancement: Launcher: preload all mods (#1352)
- Enhancement: Make save game location configurable on Android (#1337)
- Enhancement: Move the tactical screen bottom panel to the center (#1404)
- Enhancement: Option to refill totally defeated patrol groups (#1421)
- Enhancement: Refactor operations with temporary files (#135)
- Enhancement: Support an arbitrary amount of saved games (#823)
- Enhancement: Support arbitrary save game filenames (#822)
- Enhancement: Reduce direct references to item ids (#1462)
- Enhancement: File open speedup (#1402)
- Enhancement: Read and write to a proper temporary directory (#1374)
- Enhancement: Add JSON schema for all externalized files (#1422)
- Maintenance: 0.19 release checklist (#1356)
- Maintenance: AppImage does not start in Debian 10 => libstdc++.so.6: version `GLIBCXX_3.4.26' not found (#1360)
- Maintenance: CI-build with gcc-8 (#1361)
- Maintenance: Compiling JA2S 0.18 with Raspberry Pi failed (#1436)
- Maintenance: Fix C4099 warning on MSVC (#1403)
- Maintenance: Replace references to profileID in externalized JSON with profile name (#1453)
- Maintenance: VfsFile_open performance (#1268)
- Maintenance: Add editorconfig (#1460)
- Maintenance: Install CMake 3.21 for MinGW builds (#1455)
- Maintenance: DefaultContentManager::loadTranslationTable skipping some languages (#1475)
- Maintenance: Fix translation tables (#1454)
- Maintenance: Read tilecache names from VFS (#1363)
- Maintenance: Refactor the rest of file accesses to go through GCM where applicable (#1401)
- Maintenance: Remove explicit paths from DefaultContentManager startup (#1358)
