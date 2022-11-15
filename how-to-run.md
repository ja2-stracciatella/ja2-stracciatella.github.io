---
layout: page
permalink: /how-to-run/
---

- [Install](#install)
- [Configuration](#configuration)

## Install

All the options below require the **original Jagged Alliance 2 game** on your device. Make sure you do a full, clean install. If you have a game with the 1.13 mod installed, it will not work.

The original game can be obtained through

- GOG: [Jagged Alliance 2](https://www.gog.com/en/game/jagged_alliance_2)
- Steam: [Jagged Alliance 2 Gold](https://store.steampowered.com/app/1620/Jagged_Alliance_2_Gold/)
- Steam: [Jagged Alliance 2 Wildfire](https://store.steampowered.com/app/215930/Jagged_Alliance_2__Wildfire/)
  - The original game files will be in the `JA2Classic` subdirectory, not in the `Game` subdirectory
  - JA2 Stracciatella currently does not support Wildfire itself, only the [Wildfire maps through a mod](https://github.com/ja2-stracciatella/mod-wildfire-maps)
- Buying CDs (if you can find someone who wants to sell)

Follow the instructions for your platform to install JA2 Stracciatella:

<div id="accordion">
  <div class="card">
    <div class="card-header" id="heading-windows-installer">
      <a data-toggle="collapse" data-target="#collapse-windows-installer" aria-expanded="false" aria-controls="collapse-windows-installer" href="javascript:">
         Windows installer
      </a>
    </div>
    <div id="collapse-windows-installer" class="collapse" aria-labelledby="heading-windows-installer" data-parent="#accordion">
      <div class="card-body">
        <ol>
           <li>
               <p><a href="/download" target="_blank">Download the installer</a> and install Stracciatella wherever you want. Make sure to uninstall any previous version first if you want to avoid conflicts.</p>
           </li>
           <li>
               <p>Run Stracciatella from the start menu. This should bring up the launcher.</p>
           </li>
           <li>
               <p>Change <code>JA2 Game Directory</code> to the directory where your original game files are located.</p>
           </li>
           <li>
               <p>Select the game version of your original game files, or click the "Guess Game Version" button to have the launcher auto-detect it for you.</p>
           </li>
           <li>
               <p>Adapt other settings to your liking in the <code>Data</code>, <code>Mods</code> and <code>Settings</code> tab.</p>
           </li>
           <li>
               <p>Start the game in the <code>Play</code> tab.</p>
           </li>
        </ol>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="heading-windows-zip">
      <a data-toggle="collapse" data-target="#collapse-windows-zip" aria-expanded="false" aria-controls="collapse-windows-zip" href="javascript:">
         Windows ZIP
      </a>
    </div>
    <div id="collapse-windows-zip" class="collapse" aria-labelledby="heading-windows-zip" data-parent="#accordion">
      <div class="card-body">
        <ol>
           <li>
               <p><a href="/download" target="_blank">Download the ZIP</a> and extract it wherever you want. Do not extract it in the original game directory.</p>
           </li>
           <li>
               <p>Navigate to the Stracciatella directory and run <code>ja2-launcher.exe</code>. This should bring up the launcher.</p>
           </li>
           <li>
               <p>Change <code>JA2 Game Directory</code> to the directory where your original game files are located.</p>
           </li>
           <li>
               <p>Select the game version of your original game files, or click the "Guess Game Version" button to have the launcher auto-detect it for you.</p>
           </li>
           <li>
               <p>Adapt other settings to your liking in the <code>Data</code>, <code>Mods</code> and <code>Settings</code> tab.</p>
           </li>
           <li>
               <p>Start the game in the <code>Play</code> tab.</p>
           </li>
        </ol>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="heading-linux">
         <a data-toggle="collapse" data-target="#collapse-linux" aria-expanded="false" aria-controls="collapse-linux" href="javascript:">
            Linux
        </a>
    </div>
    <div id="collapse-linux" class="collapse" aria-labelledby="heading-linux" data-parent="#accordion">
      <div class="card-body">
        <ol>
           <li>
               <p><a href="/download" target="_blank">Download the AppImage</a> and put it whereever you want.</p>
           </li>
           <li>
               <p>Make the AppImage executable, either using your file manager or <code>chmod +x</code>.</p>
           </li>
           <li>
               <p>Execute the AppImage. This should bring up the Stracciatella launcher.</p>
           </li>
           <li>
               <p>Change <code>JA2 Game Directory</code> to the directory where your original game files are located.</p>
           </li>
           <li>
               <p>Select the game version of your original game files, or click the "Guess Game Version" button to have the launcher auto-detect it for you.</p>
           </li>
           <li>
               <p>Adapt other settings to your liking in the <code>Data</code>, <code>Mods</code> and <code>Settings</code> tab.</p>
           </li>
           <li>
               <p>Start the game in the <code>Play</code> tab.</p>
           </li>
        </ol>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="heading-macos">
         <a data-toggle="collapse" data-target="#collapse-macos" aria-expanded="false" aria-controls="collapse-macos" href="javascript:">
            macOS
        </a>
    </div>
    <div id="collapse-macos" class="collapse" aria-labelledby="heading-macos" data-parent="#accordion">
      <div class="card-body">
        <ol>
           <li>
               <p><a href="/download" target="_blank">Download the macOS dmg</a> and open it.</p>
           </li>
           <li>
               <p>Drag the Stracciatella app into the <code>Applications</code> folder.</p>
           </li>
           <li>
               <p>Control-click the app icon in the <code>Applications</code> folder, then choose <code>Open</code> from the shortcut menu. This only needs to be done once and should bring up the Stracciatella launcher.</p>
           </li>
           <li>
               <p>Change <code>JA2 Game Directory</code> to the directory where your original game files are located.</p>
           </li>
           <li>
               <p>Select the game version of your original game files, or click the "Guess Game Version" button to have the launcher auto-detect it for you.</p>
           </li>
           <li>
               <p>Adapt other settings to your liking in the <code>Data</code>, <code>Mods</code> and <code>Settings</code> tab.</p>
           </li>
           <li>
               <p>Start the game in the <code>Play</code> tab.</p>
           </li>
        </ol>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="heading-android">
         <a data-toggle="collapse" data-target="#collapse-android" aria-expanded="false" aria-controls="collapse-android" href="javascript:">
            Android
        </a>
    </div>
    <div id="collapse-android" class="collapse" aria-labelledby="heading-android" data-parent="#accordion">
      <div class="card-body">
        <p>
          <span class="fa fa-lg fa-info"></span>&nbsp;&nbsp;The Android app is currently not available through any store. You need to install the APK manually. Please inform yourself about allowing app installations from unknown sources for your device.
        </p>
        <ol>
           <li>
               <p>Copy the original game files to your Android device. This can be done by copying it to your device using USB or a cloud storage provider.</p>
           </li>
           <li>
               <p><a href="/download" target="_blank">Download the Android APK</a> and install it.</p>
           </li>
           <li>
               <p>Open the app. This should bring up the Stracciatella launcher.</p>
           </li>
           <li>
               <p>Change <code>JA2 Game Directory</code> to the directory where your original game files are located.</p>
           </li>
           <li>
               <p>Select the game version of your original game files. Usually this is just the language your original game is in.</p>
           </li>
           <li>
               <p>Although optional, it is recommended to set the save game directory to a directory that is accessible for other apps as well. Otherwise your save games will be deleted when you uninstall the app.</p>
           </li>
           <li>
               <p>Start the game with the button in the bottom right corner.</p>
           </li>
        </ol>
      </div>
    </div>
  </div>
</div>
<p></p>

## Configuration

### Configuration File

The configuration file will be created on the first start of the application. It is located in

- `%USERPROFILE%\Documents\JA2\ja2.json` on Windows.
- `~/.ja2/ja2.json` on Linux, BSD or macOS.
- `/data/data/io.github.ja2stracciatella/ja2.json` on Android, in the apps data directory. Usually not accessible by other apps.

### Savegame directory

The savegame directory can be changed, for example to synchronize savegames with the cloud. By default the save games are located in

- `%USERPROFILE%\Documents\JA2\SavedGames` on Windows.
- `~/.ja2/SavedGames` on Linux, BSD or macOS.
- `/data/data/io.github.ja2stracciatella/SavedGames` on Android, in the apps data directory. Usually not accessible by other apps.

### Resolution and Scaling Mode

The internal resolution lets you define how large **the tactical screen** is rendered. All other game screens are still rendered in the original `640x480` resolution and centered on the screen.

In order to increase the size of the game window, you can either resize it with the window controls, or enable fullscreen.

Scaling mode will determine how the internal resolution is scaled to your window.



**For even more configuration options check the [modding](/mods/) page.**
