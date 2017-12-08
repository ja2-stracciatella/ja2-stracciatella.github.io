---
layout: home
---

## Features

### High Resolution Support

Added support for high video resolutions. For example, game can be started in 1680x1050  mode like this: `ja2.exe -res 1680x1050`.

![Ja2 Stracciatella in 1680x1050 resolution](/img/features/high-res.jpg)

### GUI Launcher (added in 0.16.0)

A GUI Launcher is included to facilitate changing settings and tweaking the game.
![JA2 Stracciatella launcher](https://user-images.githubusercontent.com/775439/32501231-c762e246-c3d7-11e7-9f41-143ccf88dead.png)

### Dead is Dead mode (added in 0.16.0)

Dead is Dead is a new game mode for players looking for a new challenge, and who think IronMan doesn't cut it just yet. With the Dead is Dead mode the game takes the burden of saving and savegame management from your shoulders so you can concentrate on the important bits. 

You select one savegame slot at the beginning of a new game, and the game will stick to that slot throughout your playthrough. The game will also make sure to save before you leave, so you can rest assured you will always be able to pick up at where you left.

With Dead is Dead there is no going back. If mercs die, there is no way of bringing them back. If you make a mistake, there is no way of reverting it. So be careful, play it safe, and prepare to be frustrated.

### Bundled optional mini-mods (added in 0.16.0)

A few data-altering [mods](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/assets/mods) are included, but must be explicitly selected to be used:
- Generous Rebels, From Russia With Love: extra items in Omerta
- Honest IMP quiz questions: the satirical answers now include the personality aspect that they would contribute to
- O Fortuna: dramatic intro music for Jagged Alliance 2

```
    -mod MOD_NAME       Start one of the game modifications. MOD_NAME is the
                        name of modification, e.g. 'from-russia-with-love. See
                        assets/mods folder for possible options'.
```

### Integrated Editor

The map editor is now integrated into the game. Start it through the launcher or like this: `ja2.exe -editor`.

![Ja2 Stracciatella Editor](/img/features/integrated-editor.jpg)

## How to Contribute

The best way to contribute is to make a pull request with a bug fix. Please see list of open issues [here](https://github.com/ja2-stracciatella/ja2-stracciatella/issues).

The second best way is to file a bug report if you encounter a bug or help with retesting issues [where we need more info](https://github.com/ja2-stracciatella/ja2-stracciatella/labels/retest).
