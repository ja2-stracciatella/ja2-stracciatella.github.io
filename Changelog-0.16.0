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

