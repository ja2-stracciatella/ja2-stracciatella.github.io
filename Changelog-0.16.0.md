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
- Comments have been added to the configuration file making it easier to tweak.
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
 - Bugfix (vanilla): Do not increase shots fired statistic without a live target (#622)
 - Bugfix (vanilla): Bobby Rays: Popup 'Out of Stock' appearing again when trying to leave the website (#534)
 - Bugfix (vanilla): Gas on a roof can damage the merc underneath the roof (#477)
 - Bugfix (vanilla): Open doors can block grenades (#94)
 - Bugfix (vanilla): Smoke/Gas spreads over roof edge (#600)
 - Bugfix (vanilla): Climbing makes mercs visible at night (#402)
 - Bugfix (vanilla): Throwing knife flying animation messed up (#395)
 - Bugfix (vanilla): Helicopter is ignored by pathfinding (#317)
 - Bugfix (vanilla): Area select rectangle not removed if interrupted (#550)
 - Bugfix (vanilla): Replace non-existing corpse animation (#526)
 - Bugfix (vanilla): Replace reference to non-existing flame animation (#525)
 - Bugfix (vanilla): Sound file exception: doorcr_b.wav (#520)
 - Bugfix (vanilla): Game crash when inserting ceramic plates (#516)
 - Bugfix (vanilla): Unconscious merc gains exp for bullet avoidance (#163)
 - Bugfix (vanilla): Free disk space is calculated wrong (#413)
 - Bugfix: Game speed is generally slow (#99)
 - Bugfix: Don't crash if we don't have a target for punching (#627)
 - Bugfix: Don't crash in SoundLoadDisk() on Arch Linux with SDL2 2.0.6 (#608)
 - Bugfix: Sound memory limit hit after upgrading to SDL 2.0.7 (#609)
 - Bugfix: The rust cli parser does not accept relative paths (#559)
 - Bugfix: Getting "Reading from file failed" when fast forwarding time after savegame load (#528)
 - Bugfix: Crash in laptop AND huge memory footprint (#68)
 - Bugfix: Adding money with '+' key cheat not working? (#426)
 - Bugfix: Hit by grenade issues (#247)
 - Bugfix: MERCS can punch through open doors (#595)
 - Bugfix: Attack for 0 AP (#192)
 - Bugfix: Cheat: alt+o damages bloodcats now (#583)
 - Bugfix: Passive bloodcat ambush fix (#584)
 - Bugfix: When enemy is noticed, no AP for action may be taken (#188)
 - Bugfix: Attacking teammate(dialogue) on roof puts him through the roof (#567)
 - Bugfix: Mysteriously disappearing APs when stealing (#191)
 - Bugfix: Position of Mercenary task orders in Tactical screen (#537)
 - Bugfix: Fix and enhance cli switch parsing (#515)
 - Bugfix: Maximum militia Message at the wrong position (#540)
 - Bugfix: Build fails if there is a space in the directory name (#529)
 - Bugfix: Shrink gfKeyState (alternative) (#523)
 - Bugfix: Teach (Estimate)ActionPoints about KID_SKIPPING (#502)
 - Bugfix: Segfault in Blt8BPPDataTo16BPPBufferTransZTranslucent when rendering smoke (#468)
 - Bugfix: AI deadlocks (#466)
 - Bugfix: Experience gain not acknowledged properly (#398)
 - Bugfix: Minimap flickering on selected merc (#202)
 - Bugfix: Fix current merc in minimap flickering (#452)
 - Bugfix: Check for time accelleration properly when checking for end of turn (#451)
 - Bugfix: Accelerated bleeding when returning to realtime (#160)
 - Bugfix: Graphical glitch in main menu after quitting a game (#106)
 - Bugfix: Fix menu bug when ending a game (#72)
 - Bugfix: Can't type IMP code after saving via Save screen (#419)
 - Bugfix: Fix issues with text inputs (#429)
 - Bugfix: Game crashes during enemy turn (#415)
 - Bugfix: Description box missing when opening "Deposit/Withdraw money" widget in Tactical screen (#379)
 - Bugfix: Shipping cost BR not redrawn properly (#394)
 - Bugfix: Bad Performance in OS X (#319)
 - Bugfix: Fix autoresolve crash (#381)
 - Bugfix: Only check retreat conditions for valid sectors (#374)
 - Bugfix: Enable assertive asserts only on debug builds (#373)
 - Bugfix: Show version number in main menu (#359)
 - Bugfix: Fix minor debug page fault (#337)
 - Bugfix: Fix undefined behaviour in LOS.cc (#342)
 - Bugfix: Leave running stance if not moving (#194)
 - Enhancement (vanilla): Merc forgets his stance after jumping on a roof (#84)
 - Enhancement (vanilla): Selling attachments to Tony - strange prices (#423)
 - Enhancement (vanilla): Yellow or green star for attached Talon (#424)
 - Enhancement: Add extra item combinations (#623)
 - Enhancement: Unified hotkeys (#626)
 - Enhancement: Integrate vxx's work (#307)
 - Enhancement: Initial Launcher Implementation (#548)
 - Enhancement: Allow resizing of game window (#555)
 - Enhancement: ja2.ini: move to json (#291)
 - Enhancement: setting options in ja2.ini (#298)
 - Enhancement: Change name of the user folder? (#164)
 - Enhancement: Automated nightly builds (#442)
 - Enhancement: Add Appveyor CI (#440)
 - Enhancement: Add comments explaining game.json variables (#401)
 - Enhancement: New Game Mode Proposal: Dead is Dead (#308)
 - Enhancement: Make music modable to increase music variety (#386)
 - Enhancement: Update to SDL2 (#216)
 - Enhancement: Support Tribsoft's Linux port (#365)
 - Enhancement: Introduce cmake build system (#354)
 - Enhancement: Integrate gui_extras (#339)
 - Enhancement: Implement uninplemented stuff (#264)
 - Enhancement: Add “IMP Quiz Honest Answers” mini mod (#303)
 - Enhancement: Windowed mode: move to the next sector in tactical view. (#314)
 - Enhancement: Add “Generous Rebels” mini mod (#305)
 - Maintenance: Misc cleanup (#625)
 - Maintenance: Whitespace normalization (#556)
 - Maintenance: CMake cleanup (minimal version) (#482)
 - Maintenance: Remove #ifdef JA2 code (#471)
 - Maintenance: Remove #ifdef JA2TESTVERSION code (#472)
 - Maintenance: Remove #ifdef JA2BETAVERSION code (#470)
 - Maintenance: Reorganize source tree (#455)
 - Maintenance: Update rapidjson to 1.1.0 and add comments to game.json (#411)
 - Maintenance: Externalize lib boost (#229)
 - Maintenance: Update boost to 1.61. (#326)
 - Maintenance: Rework debug logging (#60)
 - Maintenance: Update smacker.c (#310)
 - Maintenance: Remove WITH_MODS ifdef (#322)
 - Maintenance: Logging rework (#250)
