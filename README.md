# CNSR-vlc-viewer-addon

**An add-on for VLC media player.**

# Description

VLC plugin for real-time media censorship according to user personal settings,
using [CNSR file format](https://github.com/ophirhan/cnsr-file-format-specification).

This plugin censors categories like nudity, verbal abuse, violence and alchohol and drug consumption.
The extension is also available [here](https://addons.videolan.org/p/1537958/).

This extension is inspired by [MEDERI's "Time v3.2" vlc extension](https://addons.videolan.org/p/1154032/).

Supported OS: Windows, Linux and Mac OS.
_____________________________________________________________________________________________________

# Getting started

1. If you don't have VLC in your computer, install from [VLC](https://www.videolan.org/)
2. download the repository: press on the "CODE" green button, and choose the option: "Download zip".
![Screenshot_061221_040915_PM](https://user-images.githubusercontent.com/19567966/121777049-c8d80580-cb98-11eb-9ac7-6db63a0c518f.jpg)
3. Find your way to these two files: 
-cnsr-vlc-viewer-addon/blob/main/extensions/cnsr_ext.lua
-cnsr-vlc-viewer-addon/blob/main/intf/cnsr_intf.lua
			       
4. Access lua folder using these paths:

If you want the extension to be available for all the users of the 
computer and not only the user currently logged in choose the all users path.
    - Windows
        - `%ProgramFiles%\VideoLAN\VLC\lua` (all users)
        - `%APPDATA%\VLC\lua` (current user)
    - Linux
        - `/usr/lib/vlc/lua` (all users)
        - `~/.local/share/vlc/lua` (current user)
    - Mac OS
        - `/Applications/VLC.app/Contents/MacOS/share/lua` (all users)
        - `/Users/%your_name%/Library/Application Support/org.videolan.vlc/lua` (current user) 
  
4. Move `cnsr_ext.lua` to \lua\extensions\ folder.
5. Move `cnsr_intf.lua` to \lua\intf\ folder.
6. Start the Extension in VLC menu
    - `View > cnsr` for Windows/Linux.
    - `VLC > Extensions > cnsr` for Mac OS.
7. Configure the cnsr categories to your liking.

# For developers

1. Change the lua folder's name to `luab`.

2. Clone the repository a new folder named `lua`

3. Copy the contents of `luab` dir to `lua` dir

4. Delete `luab` dir

and that's it! you are ready to start.

# How to use cnsr files:
In order to make use of cnsr file you need to create a new file with the format as shown in `example/example_file.cnsr`.
The file name must be identical to the video name you want to play (except for the ending), and must be at the same directory as the video.

For example, if the video you want to play is: <br>
`/foo/bar/myvid.mp4` <br>
Then the cnsr file should be: <br>
`/foo/bar/myvid.cnsr` <br>

#NOTICE
- Currently there is an issue with directoris that have underscore or spaces, so please try to avoid them

