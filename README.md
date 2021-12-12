This is a collection of John Merrit's Realistic Bezels that he originally produced for Retroarch.

# Parallel MAME Repository:

I currently dedicate my time to the MAME repository, where it all started:
https://github.com/estefan3112/MAME-Realistic-Bezel-Artwork/blob/master/README.md

# Retroarch Bezel Artwork Explained

Retroarch config files are quite different to MAME, as the concept is far less flexible than in MAME. However, Retroarch bears other advantages, in particular different Cores (including Final Burn Neo), shader sophistication, and other finetuning.

If you like tweaking, look for Retroarch. For no-hassle solutions, head for something else.

![alt text](/screenshots/1942.jpg "1942 with Overlay in Retroarch/Final Burn Alpha")

# Retroarch overlays come in two parts (three files per Game):

1. Overlay and image cfg file need to be in the Overlay directory defined in Retroarch. This is different from system to system:
- Retropie: /opt/retropie/emulators/retroarch/overlays/ -> in here create folder 'arcade-bezel-overlays'
- MacOS: :~/Library/Application Support/RetroArch/overlays/ -> create your own directory, e.g. arcade-bezel-overlays
- Windows: ...
- Linux: ~/.config/retroarch/overlay/ -> in here create folder 'arcade-bezel-overlays'
The .cfg file configured here is then defined in the Game-specific config file. So if you change the above paths, you need to rewrite the path in the Game-specific config files as well.

2. The Game-specific config file provides for the necessary parameters, in particular Overlay orientation and screen size, so this file is dependent on your screen resolution. This makes it far less portable than MAME .lay files.
The files in this repository are designed for 1080p of Retropie. For my iMac (Late 2013), for example, I have to scale the values up by 1.33, and they work. For a 4k 16:9 monitor, you obviously need to double the 1080p resolution.

This will be your work.

# Location of the Game-specific config files:
- Retropie: /opt/retropie/configs/all/retroarch/config/((directory of used Retroarch core))
- MacOS: /Users/((username))/Library/Application\ Support/RetroArch/config/#directory of used Retroarch Core#/
- Windows: ...
- Linux: ~/.config/retroarch/config/#directory of used Retroarch core#

# RECOMMENDED STEPS FOR USAGE:
1. Create a new directory called arcade-bezel-overlays in the default directory of your system indicated above.
2. Take the Overlay graphic files and put them into the directory of your choice. Subdirectories are not needed.
3. Choose a Retroarch Core that you want to use with the Overlays, can be more than one.
4. Put the Game-specific config files into the respective sub-diretory of the Core.

The game should then immediately start with the Arcade Bezel. If nothing happens, recheck files (3 per game) and directories.

# MAC USERS NEED TO TAKE SPECIAL CARE:
Since Overlays are stored in this configuration, be very careful when updating Retroarch on your Mac! Always have your Overlays at a safe place, since a new Retroarch Application Bundle will overwrite your old one, including your custom Overlays!
