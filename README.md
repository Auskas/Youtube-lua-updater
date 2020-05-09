# Youtube-lua-updater
Updates the youtube lua file for playing youtube videos over VLC player in Windows and Linux.

Python version: >= 3.6 (due to the usage of f-strings)

The algorithm is the following:
1. Determines your OS (Windows and Linux friendly)
2. Looks for the location of the lua file in your OS.
3. Downloads the last available youtube.lua file at https://raw.githubusercontent.com/videolan/vlc/master/share/lua/playlist/youtube.lua
4. Replaces the original local file with the freshly downloaded one.
5. Deletes the temporary lua file in your current working directory.

Notes:
- Windows users have to run the script under the administrator right to be able to rewrite the local file.
- Linux users will be prompted to enter their root password to overwrite the file if they are not under the root privileges.
