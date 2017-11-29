---
layout: post
title: Release 0.16.0
---

The Jagged Alliance 2 Stracciatella team is proud to present a major
new release. A long time in the making, it includes several new
features, plenty of bugfixes compared to previous versions and the
original game, and more work in externalizing and cleaning up the old
code base.

Through **TODO WWW commits XX bugs were fixed, of those YY vanilla and ZZ**
unknown.

__New Features__:

- A [graphical launcher](https://ja2-stracciatella.github.io/#gui-launcher)
- “Dead is Dead” mode:
  [documentation](https://ja2-stracciatella.github.io/#dead-is-dead-mode)
- 4 new bunbled optional
  [mini-mods](https://ja2-stracciatella.github.io/#bundled-optional-mini-mods):
  Honest IMP Questions, Generous Rebels, O Fortuna, From Russia With
  Love
- The game window is now resizable, which enables software pixel scaling
- Some fixes and tweaks cherry-picked from 1.13
- Configuration is now stored in a JSON file. 
- Comments have been added to the configuration file making it easier to tweak. It is easier to find, too.
  **TODO: docs**

We are shipping pre-built packages for Ubuntu, Windows and
OS X. This should help users to easily get started with Jagged Alliance
2 Stracciatella. For users willing to take a risk we provide automatically created nightly
builds.

__Download__:
[http://ja2-stracciatella.github.io/download/](http://ja2-stracciatella.github.io/download/)

__Build changes__:
 - The build system has been updated and is now based on cmake.
 - SDL has been replaced with SDL2.
 - Several other dependencies have been updated.
 - The optional graphical launcher requires FLTK.
 - Rust has been added as a new dependency. It is recommended to use the latest version provided by rustup. Rust libraries needed to build the project are automatically downloaded by cmake/cargo.

_Warning_: **SDL2** 2.0.6 has a fatal bug in the audio conversion code. As a workaround, the game automatically disables all sounds if it detects this version during startup. Please downgrade to version 2.0.5 or use **version 2.0.7 or later**.

From the next release onward, the project will start using C++11
features. Please let us know if you're stuck with an ancient compiler that doesn't support this standard.

__Full Changelog__:

**TODO**
- Feature:
- Bugfix: End of meanwhile cutscene crash (#198)


**Page 1**
 - Game speed is generally slow (#99)
 - extra item combinations (#623)
 - Do not increase shots fired statistic without a live target (#622)
 - Misc cleanup (#625)
 - Unified hotkeys (#626)
 - Don't crash if we don't have a target for punching (#627)
 - integrate vxx's work enhancement major (#307)
 - Crash in SoundLoadDisk() on Arch Linux with SDL2 2.0.6 (#608)
 - Bobby Rays: Popup 'Out of Stock' appearing again when trying to leave the website (#534)
 - Whitespace normalization (#556)
 - Sound memory limit hit after upgrading to SDL 2.0.7 (#609)
 - Initial Launcher Implementation (#548)
 - The rust cli parser does not accept relative paths (#559)
 - Getting "Reading from file failed" when fast forwarding time after savegame load (#528)
 - Crash in laptop AND huge memory footprint (#68)
 - Adding money with '+' key cheat not working? (#426)
 - Gas on a roof can damage the merc underneath the roof (#477)
 - Open doors can block grenades (#94)
 - Hit by grenade issues (#247)
 - Smoke/Gas spreads over roof edge (#600)
 - MERCS can punch through open doors (#595)
 - Attack for 0 AP (#192)
 - Merc forgets his stance after jumping on a roof (#84)
 - Climbing makes mercs visible at night (#402)
 - Throwing knife flying animation messed up (#395)
 **Page 2**
 - Cheat: alt+o damages bloodcats now (#583)
 - Passive bloodcat ambush fix (#584)
 - Helicopter is ignored by pathfinding (#317)
 - When enemy is noticed, no AP for action may be taken (#188)
 - Attacking teammate(dialogue) on roof puts him through the roof (#567)
 - Area select rectangle not removed if interrupted (#550)
 - Mysteriously disappearing APs when stealing (#191)
 - Position of Mercenary task orders in Tactical screen (#537)
 - Fix and enhance cli switch parsing (#515)
 - Allow resizing of game window (#555)
 - Maximum militia Message at the wrong position (#540)
 - Build fails if there is a space in the directory name (#529)
 - Replace non-existing corpse animation (#526)
 - Replace reference to non-existing flame animation (#525)
 - Shrink gfKeyState (alternative) (#523)
 - Sound file exception: doorcr_b.wav (#520)
 - Game crash when inserting ceramic plates (#516)
 - Teach (Estimate)ActionPoints about KID_SKIPPING (#502)
 - Segfault in Blt8BPPDataTo16BPPBufferTransZTranslucent when rendering smoke (#468)
 - AI deadlocks (#466)
 - CMake cleanup (minimal version) (#482)
 - Experience gain not acknowledged properly (#398)
 - Remove #ifdef JA2 (#471)
 - Consider removing JA2TESTVERSION (#472)
 - JA 10 - Think about removing JA2BETAVERSION (#470)
 **Page 3**
 - ja2.ini: move to json (#291)
 - setting options in ja2.ini (#298)
 - Change name of the user folder? (#164)
 - Minimap flickering on selected merc (#202)
 - Fix current merc in minimap flickering (#452)
 - Check for time accelleration properly when checking for end of turn (#451)
 - Accelerated bleeding when returning to realtime (#160)
 - Graphical glitch in main menu after quitting a game (#106)
 - menu bug when ending a game (#72)
 - Can't type IMP code after saving via Save screen (#419)
 - Fix issues with text inputs (#429)
 - Automated nightly builds (#442)
 - Add Appveyor CI (#440)
 - Unconscious merc gains exp for bullet avoidance (#163)
 - Selling attachments to Tony - strange prices (#423)
 - Yellow or green star for attached Talon (#424)
 - Add comments explaining game.json variables (#401)
 - Update rapidjson to 1.1.0 and add comments to game.json (#411)
 - Game crashes during enemy turn non-vanilla (#415)
 - Free disk space is calculated wrong bug major vanilla (#413)
 - Description box missing when opening "Deposit/Withdraw money" widget in Tactical screen (#379)
 - New Game Mode Proposal: Dead is Dead (#308)
 - Shipping cost BR not redrawn properly (#394)
 - Request: more music variety (#386)
 - Bad Performance in OS X (#319)
 **Page 4**
 - Update to SDL2 (#216)
 - autoresolve crash (#381)
 - Only check retreat conditions for valid sectors (#374)
 - enable assertive asserts only on debug builds (#373)
 - Should it work with a copy of Tribsoft's Linux port? (#365)
 - Introduce cmake build system (#354)
 - Fix #300: Show version number in main menu (#359)
 - minor debug page fault (#337)
 - integrate gui_extras (#339)
 - Implement uninplemented stuff (#264)
 - fix undefined behaviour in LOS.cc (#342)
 - Externalize lib boost (#229)
 - Iqha mini mod (#303)
 - Update boost to 1.61. (#326)
 - Rework debug logging (#60)
 - Update smacker.c (#310)
 - Windowed mode: move to the next sector in tactical view. (#314)
 - Gr mini mod (#305)
 - Any objection to removing WITH_MODS? question (#322)
 - Logging rework (#250)
 - Running w/out moving (#194)

