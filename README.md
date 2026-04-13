# eleveneyes-xbox360-patch-releases
11eyes CrossOver localization patch releases

[How to use](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/USAGE.md)

[Menu guide](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/GUIDE.md)

# Important disclaimer
* Due to unforeseen consequences, the patch might not be able to be continued for a long time. However, you can use the method outlined at [MagesTools](https://github.com/ThePlayer14/MagesTools_en) to make the remaining scripts.

# Downloading the patch
* Download `scripts-cooked.tar.zst` and the movie patch from the Releases section and apply the patch as it's described in  [How to use](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/USAGE.md).

# What's supported by this patch?
* The `.scr` scripts that can be extracted by [MagesTools](https://github.com/ThePlayer14/MagesTools_en).
* You can edit the contents of those scripts by using MagesTools and the charset file. The charset file should be unpacked first, then it's ready to use.
* Currently, only the CrossOver storyline is fully translated in this patch.

# How to create the cinematics with the subs
The original WMV files need to be hardsubbed with the relevant Substation subtitle from the subtitle archive, re-encoded into AVI using Avidemux (or the transcoder of your choice), and then, this AVI is loaded into [Expression Encoder](https://www.videohelp.com/software/Microsoft-Expression-Encoder), selecting the `VC1 Xbox 360 720p` preset. Set Bitrate to 8000, and the audio to plain WMA, set Audio bitrate to 192k and 48.0 kHz. The output file should play inside Xenia DX12 (Windows) or a modded Xbox 360.


# Limitations of the patch
* The UI for the game cannot be localized. All UI interface BMP files, including the character atlas (`011.bmp`) are stored within the `system.dat` file, which is an LNK4 archive.
Only an unpacker named [exlnk4](https://github.com/hiroshil/asmodean-tools/tree/main/exlnk4) is known to exist, but not a packer for this format.
* Please note that this patch is an experimental one, and the Main Story segment might not be fully completed, since there might be undiscovered bugs in the script conversion process. The CrossOver segment does not exhibit this issue.

  
# Credits
* SunSubs Team and [Asahina](https://github.com/kokomif) for translation
* Charset file by John_Titor 
