---
layout: post
title: Release 0.20.0
---

The Jagged Alliance 2 Stracciatella team is proud to present a new release showcasing about half a year of work. It includes several new features, plenty of bugfixes compared to previous versions and the original game, clean-ups of the old code base, and most notably the first official release of the Android version and support for touch controls.

Through 490 commits at least 76 bugs were fixed, 20 of which are known to affect vanilla.

## New Features:
  - Touch Controls: Control your mercenaries with the touch of a finger on touch-devices
  - First Official Android Release: Play Jagged Alliance on the go on your Android device
  - Modding Improvements
    - More hardcoded values and assumptions are now externalized to additional or improved json files for easy editing in JSON: item names, item descriptions, aim and range bonuses
    - More extension points for LUA scripting: change shop inventory and prices, react to merc hiring, create message boxes
  - Stability Improvements: Fixes in memory management should lead to improved stability and less crashes

**IMPORTANT**: If you used older versions of JA2 Stracciatella on Android before you might need to uninstall them before installing the new release. Make sure to backup your data before doing this as it might erase your saves.

We are shipping pre-built packages for Linux, Windows, macOS and finally Android. This should help users to easily get started with Jagged Alliance 2 Stracciatella. For users willing to take a risk we also provide automatically created [nightly builds](https://storage.googleapis.com/ja2-builds/index.html#nightlies/).

### Download

[http://ja2-stracciatella.github.io/download/](http://ja2-stracciatella.github.io/download/)

## Main Changelog:

### Enhancements

- Enhancement: Add CMake option to compile with ASAN enabled (#1689)
- Enhancement: Add read/write functionality for STCI to rust (#1527)
- Enhancement: Allow to choose vanilla version in Android launcher (#1684)
- Enhancement: Allow using system magic_enum (#1599)
- Enhancement: Android Asset VFS layer improvements (#1248)
- Enhancement: Android launcher settings tab (#1685)
- Enhancement: Autosaving / SavegameScreen Layout (#302) (#1669)
- Enhancement: Bump string theory to fix warnings (#1486)
- Enhancement: Deprecate C-style SLOG (#1487)
- Enhancement: Does MemMan still have a purpose? (#1574)
- Enhancement: Fails to build with miniaudio-0.11.9 (#1567)
- Enhancement: Gentoo ebuilds impossible if code gets downloaded at compile time. (v.0.18.0 and later) (#1377)
- Enhancement: Instructions and credits for the simplified chinese mod (#1514)
- Enhancement: Let FindNearestEdgePoint try harder to find a suitable gridno (#1632)
- Enhancement: LUA and SOL2 may be taken from system now (#1526)
- Enhancement: Make OppList.cc more robust (#1643)
- Enhancement: Make system miniaudio use possible (#1533)
- Enhancement: README.md: improve wording (#1598)
- Enhancement: Run game without blocking the launcher and add logs as a launcher tab (#1532)
- Enhancement: Tooltips to explain about resolution and scaling modes (#1663)
- Enhancement: Touch controls (#1552)

### Modding Improvements

- Modding: Add integration points to change shop inventories and prices (#1609)
- Modding: Script extension points on new merc hired (#1672)
- Modding: Externalize item names and descriptions (#1575)
- Modding: Externalize more hardcoded values (#1541)
- Modding: Functions to make message boxes in Lua (#1614)
- Modding: Generate Lua enums from C++ codebase (#1286)

### Bugfixes (vanilla)

- Bugfix (vanilla): Can't steal weapon from enemy on roof (#1676)
- Bugfix (vanilla): Combatant counting in autoresolved combat is wrong (#1625)
- Bugfix (vanilla): Do not kill EPC twice in Auto Resolve (#1628)
- Bugfix (vanilla): Firing mode is not updated when stealing a gun (#196)
- Bugfix (vanilla): Fix FindNumTurnsBetweenDirs (#1566)
- Bugfix (vanilla): Fix helicopter run not using sound effects volume modifier (#1570)
- Bugfix (vanilla): Fix memory leak in tactical placement (#1644)
- Bugfix (vanilla): Fix rare vanilla vehicle bugs (#1522)
- Bugfix (vanilla): Fix several unrelated issues discovered by Coverity  (#1608)
- Bugfix (vanilla): Fix stealing from enemies on roof (#1677)
- Bugfix (vanilla): Fix Structure not defined warnings (#1579)
- Bugfix (vanilla): Fix the Helicopter Sound Effect at the start of the game (#1562)
- Bugfix (vanilla): Fix two more world data OOB accesses (#1638)
- Bugfix (vanilla): Fix two out of range array accesses (#1640)
- Bugfix (vanilla): If Cambria recaptured by hostiles, you will get full amount of money like it is 100% yours every day (#1670)
- Bugfix (vanilla): Keep hand item and weapon mode in sync (#1577)
- Bugfix (vanilla): MineAMine: return amount mined only if mine is controlled by player (#1673)
- Bugfix (vanilla): Possible INT8 overflow in bLockDamage (#1538)
- Bugfix (vanilla): Segfault in DistanceVisible() (#1635)
- Bugfix (vanilla): Yet another segfault in DistanceVisible() (#1634)

### Bugfixes

- Bugfix: 2 coverity fixes (#1543)
- Bugfix: Adressing some of the CIDs in NPC.cc (#1617)
- Bugfix: AIMHistory: fix not being able to move past AIM founder via Next (#1578)
- Bugfix: AI Path crash? Unable to progress. (#1569)
- Bugfix: Another crash while trying to go to Drassen Airport (#1589)
- Bugfix: Another round of Coverity fixes (#1652)
- Bugfix: Assertion failed FPS drop with display cover key (#1548)
- Bugfix: Crash when switching places with NPC (#1607)
- Bugfix: Discord link is invalid (#1597)
- Bugfix: Do not call NPCReachedDestination() for soldiers without a MercProfile (#1658)
- Bugfix: Fix #1538 Possible INT8 overflow in bLockDamage (#1554)
- Bugfix: Fix Android CI build for external contributors (#1534)
- Bugfix: Fix display of the debug pages (#1633)
- Bugfix: Fix error messages when commiting read pointer in sound system (#1546)
- Bugfix: Fix fast help active checks (#1582)
- Bugfix: Fix OOB array access in UpdatePublic (#1645)
- Bugfix: Fix seven more Coverity issues (#1637)
- Bugfix: Fix several problems detected by Memcheck (#1572)
- Bugfix: Fix the newly detected Coverity issues (#1647)
- Bugfix: Let Auto Resolve free the soldiers created for it (#1619)
- Bugfix: More coverity fixes (#1613)
- Bugfix: More Coverity fixes (#1649)
- Bugfix: More Coverity fixes (#1654)
- Bugfix: Newer Android release cant be installed over older Android release (#1503)
- Bugfix: Build signed release APKs instead of debug APKs for Android (#1518)
- Bugfix: Cannot save game anymore since v0.19.1 (#1550)
- Bugfix: Crash in Omerta when Fatima talks to Dmitri (#1581)
- Bugfix: Crash while defending Drassen Airport (#1584)
- Bugfix: Deposit/withdraw button just doesn't work (#1666)
- Bugfix: Display correct location of militia training in Finances (#1641)
- Bugfix: Do not use the c_str() result of an already destroyed ST::string (#1603)
- Bugfix: Don't try to move soldiers that are not in the sector in EndTurn() (#1585)
- Bugfix: Ensure RegisterBackgroundRect properly initializes BACKGROUND_SAVE structs (#1665)
- Bugfix: Fix Android package name (#1656)
- Bugfix: Fix bPercentCoverForGridno values going out of 0-100 bound (#1549)
- Bugfix: Fix crashes #1537 and #1559 (#1560)
- Bugfix: Fix ERROR_NOT_SAME_DEVICE for Windows (#1553)
- Bugfix: Fix incorrect schemas for weapons and item replacements (#1590)
- Bugfix: Fix indexing into m_sectorLandTypes (#1596)
- Bugfix: Fix memory leak in EmptyDialogueQueue() (#1655)
- Bugfix: Fix OOB in AIMHistory (#1605)
- Bugfix: Fix some remaining invalid format strings for sectors (#1573)
- Bugfix: Fix SwapMercPositions logic (#1611)
- Bugfix: Graphical corruption (#1661)
- Bugfix: Handle the EXDEV error on all OS's where it can happen (#1530)
- Bugfix: Ice Cream truck out of fuel crash? (#1537)
- Bugfix: Let enemy soldiers climb onto roofs again (#1615)
- Bugfix: Rapidly right clicking stacked items exits with code -1073741819 (#1679)
- Bugfix: Restore the save game validity condition from before sector refactoring (#1563)
- Bugfix: Touch control fixes (#1682)
- Bugfix: Repeatable crash when opening tactical view in sector after game load (#1657)
- Bugfix: RUNTIME ERROR in Drassen Airport (#1588)
- Bugfix: Several more coverity fixes (#1544)
- Bugfix: Silence rapidjson build warnings (#1540)
- Bugfix: Skyrider crashes the game on my current progress (#1559)
- Bugfix: Store state for whom assignment menu is shown separately (#1692)

### Maintenance Work

- Maintenance: 0.20 release checklist (#1680)
- Maintenance: Remove Debug.cc (#1488)
- Maintenance: Add bugfix release branch filter for appveyor (#1529)
- Maintenance: Cleanup clang compiler warnings (#1688)
- Maintenance: Cleanup KEY_ON_RING related code (#1561)
- Maintenance: Cmake: pass -Wno-deprecated-declarations to silence rapidjson #1540 (#1555)
- Maintenance: Cmake: rewrite the contributor tracking target (#1520)
- Maintenance: Coverity: enable asserts (#1621)
- Maintenance: Coverity_model: remove redundant model [ci skip] (#1636)
- Maintenance: Coverity: properly pass a cmake define [ci skip] (#1629)
- Maintenance: Debug: another attempt at avoiding asserting coverity reports (#1616)
- Maintenance: DefaultContentManager::loadTranslationTable: remove unused variable (#1528)
- Maintenance: Do not use abs() before hypot() (#1630)
- Maintenance: Do no update sight values in DecaySmokeEffects and DecayLightEffects (#1583)
- Maintenance: Encapsulate sectors v2 (#1479)
- Maintenance: Fix several incorrect gridno comparisons (#1622)
- Maintenance: Get rid of ndk fork in rust dependencies (#1519)
- Maintenance: New implementation of atan8 (#1565)
- Maintenance: New release? (#1660)
- Maintenance: Options to build with or without magic_enum (#1667)
- Maintenance: Overhaul Animation_Cache (#1571)
- Maintenance: Rapidjson: silence -Wclass-memaccess warnings #1486 (#1525)
- Maintenance: Remove Debug.cc #1488  (#1523)
- Maintenance: Remove Logger.cc (#1564)
- Maintenance: Remove MemMan.h and MemMan.cc (#1576)
- Maintenance: Remove the MouseRegion::Base hack (#1683)
- Maintenance: Small cleanups (#1551)
- Maintenance: Store BACKGROUND_SAVE structs in a forward_list (#1586)
- Maintenance: Try to avoid false positives from coverity scans (#1610)
- Maintenance: Unify SLOG (#1524)
- Maintenance: Upgrade Android dependencies and clean up deprecations (#1642)
- Maintenance: Upgrade Android NDK to r25 (#1639)
- Maintenance: Upgrade included miniaudio to 0.11.9 (#1568)
- Maintenance: Upgrade included SDL to 2.0.20 (#1515)
- Maintenance: Upgrade miniaudio dependency to latest version in 0.10.x branch (#1531)
- Maintenance: Upgrading googletest to v1.11 (#1668)
- Maintenance: Use standard functions instead of macros and reimplementations (#1502)
