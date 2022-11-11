---
layout: page
permalink: /features/
title: "Features"
---

Stracciatella walks a fine line between preserving the original gameplay, adding ease-of-life
improvements and providing new inobtrusive optional features.

  - [GUI Launcher](#gui-launcher)
  - [High Resolution Support](#high-resolution-support)
  - [Extra Hotkeys](#extra-hotkeys)
  - [Dead is Dead mode](#dead-is-dead-mode)
  - [Infinite save games](#infinite-save-games)
  - [Better modding support](#better-modding-support)
  - [Wildfire support](#wildfire-support)
  - [Integrated Editor](#integrated-editor)
  - [Debug screens](#debug-screens)

On the internal side, good code as-a-feature has been a major focus of the project, easily
illustrated by comparing the amount of code in related engines (as of March 2021):

<table>
  <thead>
    <tr>
      <th>Engine</th>
      <th>Lines of code</th>
      <th>Difference</th>
      <th>Languages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Original JA2</td>
      <td style="text-align: right;">1,222,384</td>
      <td style="text-align: center;">-</td>
      <td>C</td>
    </tr>
    <tr>
      <td><strong>Stracciatella</strong></td>
      <td style="text-align: right;">851,152</td>
      <td style="text-align: center;">-30,4 %</td>
      <td>C++, Rust, (LUA)</td>
    </tr>
    <tr>
      <td>JA2 1.13</td>
      <td style="text-align: right;">2,184,310</td>
      <td style="text-align: center;">+78,7 %</td>
      <td>C++, (LUA)</td>
    </tr>
  </tbody>
</table>


## GUI Launcher
*Note: added in 0.16.0.*

A GUI Launcher is included to facilitate changing settings and tweaking the game.
<img src="/img/features/launcher-tab1.jpg" style="max-width: 32.5%" alt="JA2 Stracciatella launcher tab 1">
<img src="/img/features/launcher-tab2.jpg" style="max-width: 32.5%" alt="JA2 Stracciatella launcher tab 2">
<img src="/img/features/launcher-tab3.jpg" style="max-width: 32.5%" alt="JA2 Stracciatella launcher tab 3">


## High Resolution Support

Added support for high video resolutions. For example, game can be started in 1680x1050  mode like this: `ja2.exe -res 1680x1050`.

<img src="/img/features/high-res.jpg" style="max-width: 50%" alt="JA2 Stracciatella in 1680x1050 resolution">


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

These require you toggle a [game.json](mods.md) switch:
- d: switch to turnbased mode from realtime

Additionally you can use the middle mouse button to make a merc look into the direction of the cursor.


## Dead is Dead mode
*Note: added in 0.16.0.*

Dead is Dead is a new game mode for players looking for a new challenge, and who think Iron Man doesn't cut it just yet. With the Dead is Dead mode the game takes the burden of saving and savegame management from your shoulders so you can concentrate on the important bits.

You select one savegame slot at the beginning of a new game, and the game will stick to that slot throughout your playthrough. The game will also make sure to save before you leave, so you can rest assured you will always be able to pick up at where you left.

With Dead is Dead there is no going back. If mercs die, there is no way of bringing them back. If you make a mistake, there is no way of reverting it. So be careful, play it safe, and prepare to be frustrated.


## Infinite save games

The engine now supports saving and loading of arbitrarily named saved games, and an arbitrary number of them.
The load screen is enhanced with game mode, difficuly and mod info plus a scrollbar.

<img src="/img/features/new_saveload.jpg" style="max-width: 50%" alt="JA2 Stracciatella's enhanced load screen">


## Better modding support
Mods are easier to make and users are empowered to tweak the game themselves. See our dedicated page on modding and available [mods](mods.md).

To use one of the mods, enable them in the launcher or pass the `-mod` flag on the command line.


## Wildfire support
*Note: added in 0.17.0.*

Basic Wildfire support is present, with most of the data differences externalized. You need
to have JA2, Wildfire and [this conversion](https://github.com/ja2-stracciatella/mod-wildfire-maps/releases)
installed to start a Wildfire game. It is implemented as other [mods](#bundled-optional-mini-mods), so you can
still play vanilla games too.

Read the included [README](https://github.com/ja2-stracciatella/mod-wildfire-maps/blob/master/README.md)
for detailed instructions and caveats.


## Integrated Editor

The map editor is now integrated into the game. Start it through the launcher or like this: `ja2.exe -editor`.

<img src="/img/features/integrated-editor.jpg" style="max-width: 50%" alt="JA2 Stracciatella Editor">


## Debug screens
*Note: added in 0.15.0.*

Some debug screens are accessible when using the `-debug` parameter.

Tactical Screen:

- `F11` for Quest Debug Screen
- `CTRL+f` for FPS Display
- `CTRL+z` to toggle z-buffer
- `ALT+m` for level node debug mode
- `ALT+n` to play quotes of hovered merc
- `q` for soldier and land debug mode
- `y` for struct debug mode

To exit any screen press `q`. To cycle through different pages use `pageup` and `pagedown`.

Examples:

<img src="/img/features/debug-soldier.png" style="max-width: 49%" alt="Debug soldier">
<img src="/img/features/debug-land.png" style="max-width: 49%" alt="Debug land">
<img src="/img/features/debug-z-buffer.png" style="max-width: 49%" alt="Debug z-buffer">
