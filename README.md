# eleveneyes-xbox360-patch-releases
11eyes CrossOver localization patch releases

[How to use](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/USAGE.md)

[Menu guide](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/GUIDE.md)

# Downloading the patch
* Download `scripts-cooked.tar.zst` and the movie patch from the Releases section and apply the patch as it's described in  [How to use](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/USAGE.md).

# What's supported by this patch?
* The `.scr` scripts that can be extracted by [MagesTools](https://github.com/ThePlayer14/MagesTools_en).
* You can edit the contents of those scripts by using MagesTools and the charset file. The charset file should be unpacked first, then it's ready to use.
* Currently, only the CrossOver storyline is fully translated in this patch, but stay tuned for updates for the main storyline, which will gradually get released.

# Limitations of the patch
* The UI for the game cannot be localized. All UI interface BMP files, including the character atlas (`011.bmp`) are stored within the `system.dat` file, which is an LNK4 archive.
Only an unpacker named [exlnk4](https://github.com/hiroshil/asmodean-tools/tree/main/exlnk4) is known to exist, but not a packer for this format.
* Please note that this patch is an experimental one, and the Main Story segment might not be fully completed, since there might be undiscovered bugs in the script conversion process. The CrossOver segment does not exhibit this issue.  
# Credits
* SunSubs Team and [Asahina](https://github.com/kokomif) for translation
* Charset file by John_Titor 
