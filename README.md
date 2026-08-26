# eleveneyes-xbox360-patch-releases
11eyes CrossOver localization patch releases

[How to use](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/USAGE.md)

# Important disclaimer
* Due to unforeseen consequences, the patch might not be able to be continued for a long time. However, you can use the method outlined at [MagesTools](https://github.com/ThePlayer14/MagesTools_en) to make the remaining scripts.

# Downloading the patch
* Download `scripts-cooked.tar.zst` and the movie patch from the Releases section and apply the patch as it's described in  [How to use](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/USAGE.md).

# What's supported by this patch?
* The `.scr` scripts that can be extracted by [MagesTools](https://github.com/ThePlayer14/MagesTools_en).
* You can edit the contents of those scripts by using MagesTools and the charset file. Use the "despacer" version of the charset for proper "space" insertion. The charset file should be unpacked first, then it's ready to use.
* Currently, only the CrossOver storyline is fully translated in this patch.
* UI translation patch is now available. Get it from the Releases section.

# How to create the cinematics with the subs
The original WMV files need to be hardsubbed with the relevant Substation subtitle from the subtitle archive, re-encoded into AVI using Avidemux (or the transcoder of your choice), and then, this AVI is loaded into [Expression Encoder](https://www.videohelp.com/software/Microsoft-Expression-Encoder), selecting the `VC1 Xbox 360 720p` preset. Set Bitrate to 8000, and the audio to plain WMA, set Audio bitrate to 192k and 48.0 kHz. The output file should play inside Xenia DX12 (Windows) or a modded Xbox 360.

# Picking up the project
If you'd like to pick up the project, grab the script archive, which has the raw, untranslated and text-converted sources for all the scripts that were in the original SCR files.

If you're looking to pick up the Original Story segment, continue at `SC045`.

# Remarks
* Originally, the UI for the game couldn't be localized. All UI interface BMP files, including the character atlas (`011.bmp`) are stored within the `system.dat` file, which is an LNK4 archive.
~~Only an unpacker named [exlnk4](https://github.com/hiroshil/asmodean-tools/tree/main/exlnk4) is known to exist, but not a packer for this format.~~ 
This is no longer the case since there's a [Python tool](https://github.com/ThePlayer14/LNK4tool_aio) that can handle both extraction and packing.  
If you're looking for the menu guide as a reference, here it is: [Menu guide](https://github.com/ThePlayer14/eleveneyes-xbox360-patch-releases/blob/main/GUIDE.md)
* It is possible to splice in characters into the atlas file (`011.png`). However you need to test if your insertions are showing up correctly, and also, if you splice in new characters in the atlas file, make sure to add them into the charset file you're using.
* It's also possible to create atlases using charset files via [mgsfontgen-dx_py](https://github.com/ThePlayer14/mgsfontgen_dx-python) with specific settings (64 columns, font size 28, MS PGothic), however, your mileage may wary with other fonts / settings.

    However, you might need to tweak the original "despacer" charset file to add in characters present in `011.png` that are not in the "despacer" file. Note that the tweaked charset is only useful for          "display" purposes, trying to use it as a charset file for decoding / encoding will likely result in a garbled output.

* Please note that this patch is an experimental one, and the Main Story segment might not be fully completed, since there might be undiscovered bugs in the script conversion process. The CrossOver segment does not exhibit this issue.

  
# Credits
* SunSubs Team and [Asahina](https://github.com/kokomif) for translation
* Charset file by John_Titor 
