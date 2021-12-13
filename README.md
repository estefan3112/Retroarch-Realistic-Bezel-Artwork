This is a collection based on John Merrit's Realistic Bezels that he originally produced for RetroPie.
Main contributions of this repository:
- This is mainly for RetroArch MacOS, but with a correction of the path in the game .cfg, it works on any OS.
- I remove the scratch screens (you can have them in my MAME repo switched on and off).
- I add decent screen bezels and screen masks as layers and merge them into one PNG (example: 1943).
- I add single bezels from other producers, such as Orion's Angel (e.g. Alien Syndrome).
- Only unchanged bezels of John Merrit will stay.
This is strictly non-commercial work.

## UPDATE 2021: a fresh start for my Mac
On my M1 Mac, Retroarch Metal gives me the best Arcarde experience. I started to refresh the overlays stored here, but it will be a long and tedious work. Whenever you find a new configuration file in the Mac Config folder, you can expect a refreshed overlay in the overlay diretory as well.

**Why are all vertical bezels rotated by +/-90 degree?**

It's a thing I needed to do for FinalBurn Neo in RetroArch. I did not find a better solution.

### Note - parallel MAME Repository:
Here is my repository for MAME, where it all started:
https://github.com/estefan3112/MAME-Realistic-Bezel-Artwork/blob/master/README.md

# Retroarch Bezel Artwork Explained

Retroarch config files are quite different to MAME, as the concept is far less flexible. However, Retroarch bears other advantages, in particular different Cores (including Final Burn Neo), shader sophistication, and other finetuning.

If you like tweaking, look for Retroarch. For no-hassle solutions, head for something else.

![alt text](/screenshots/1943.jpeg "1943 with Overlay in Mac Metal Retroarch/Final Burn Neo on 4K monitor")
![alt text](/screenshots/berzerk.jpeg "Berzerk with Overlay in Mac Metal Retroarch/Final Burn Neo on 4K monitor")

## Retroarch overlays come in two parts (three files per Game):

1. Overlay and image cfg file need to be in the Overlay directory defined in Retroarch. This is different from system to system:
- Retropie: /opt/retropie/emulators/retroarch/overlays/ -> in here create folder 'arcade-bezel-overlays'
- MacOS: :~/Library/Application Support/RetroArch/overlays/ -> create your own directory, e.g. here '00-realisticbezels'
- Linux: ~/.config/retroarch/overlay/ -> in here create folder 'arcade-bezel-overlays'
The .cfg file configured here is then defined in the Game-specific config file. So if you change the above paths, you need to rewrite the path in the Game-specific config files as well.

2. The Game-specific config file provides for the necessary parameters, in particular Overlay orientation and screen size, so this file is dependent on your screen resolution. This makes it far less portable than MAME .lay files.
The files in this repository are designed for 1080p of Retropie. For my iMac (Late 2013), for example, I have to scale the values up by 1.33, and they work. For a 4k 16:9 monitor, you obviously need to double the 1080p resolution.
This will be your work.

## Location of the Game-specific config files:
- Retropie: /opt/retropie/configs/all/retroarch/config/((directory of used Retroarch core))
- MacOS: /Users/((username))/Library/Application\ Support/RetroArch/config/#directory of used Retroarch Core#/
- Linux: ~/.config/retroarch/config/#directory of used Retroarch core#

## RECOMMENDED STEPS FOR USAGE:
1. Create a new directory in the default directory of your system indicated above.
2. Take the overlay graphic files and put them into the directory of your choice. Subdirectories are not needed.
3. Choose a Retroarch Core that you want to use with the Overlays, can be more than one.
4. Put the Game-specific config files into the respective sub-diretory of the Core.

The game should then immediately start with the Arcade Bezel. If nothing happens, recheck files (3 per game) and directories.

## MAC USERS: OVERLAYS NO LONGER IN APP BUNDLE:
Good to see that RetroArch has moved the overlay data out of the app bundle into the Application Support directory. Of course you could always configure this differently, but it's much better to have this now as a standard directory.
