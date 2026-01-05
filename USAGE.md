# How to use this patch 
* PC / Xenia: Use the Windows build of Xenia Canary, the Vulkan one is incomplete and will freeze on the cinematics (even on unmodded versions loaded from ISO).

  Make sure you have an ISO or a GoD dump you can use for the next steps.

  If you have an ISO, you can use [xdvdfs](https://github.com/antangelo/xdvdfs) to extract the ISO using `xdvdfs unpack ./disc.iso`, it will extract the ISO contents into a folder with the same name as the disc.

  If you have a GoD dump. you will have a file named like `04e043a24d53f6ae99313e825c6eedeabb9aec83` and folder named `04e043a24d53f6ae99313e825c6eedeabb9aec83.data` (if you downloaded it from the CDN).

  To convert GoD to an ISO file, you can use [God2Iso](https://github.com/raburton/god2iso) and extract it using `xdvdfs` as mentioned above. Note that is advised to rename the GoD file and its folder to a shorter name like `465607D4`.

  Once extracted, you should have a folder named `$SystemUpdate`, `data`, a file named `default.xex`, and an STFS container `nxeart`. your focus is on the `data` folder.
# Extraction of the files into the data folder
  * Within the `data` folder, there's the LNK4 `.dat` files (which cannot be localized / repacked), the `.afs` files, and 4 WMV files, and a `script` folder.

    The cinematics are the WMV files, and to non-destructively replace them, simply just rename them by appending either `.bak` or `.old` or `.org` (original) to the end of the file, so it should be like `op01.wmv.org` or the extension of your choice.

    Once done, just paste the contents of the movie patch into the directory.

    For the scripts, you can do the same steps, download them from the the repo base, rename original scripts using the same non-destructive method as above, it should look like `SC000.scr.org` or `SX001.scr.org`.

    Once done, you can launch Xenia Canary by opening `default.xex`, and the game should load the custom files.
# How to use the patch on real hardware (advanced)
Depending on your console version, this might vary. I've tested it on a Xbox 360 Slim with a Trinity motherboard.

Create a fully new user profile, and disable automatic login if it's set up on a profile.

Use either the [360HackPack](https://github.com/alex-free/360-hack-pack) or [BadBuilder](https://github.com/Pdawg-bytes/BadBuilder) to create a Bad Update USB stick. To get the RB-Blitz trial you can get it from [here](https://archive.org/details/rbblitz-trial).

Note that your USB drive needs to be formatted using MBR partition table and `fat32` in order to be used on the Xbox 360 as a storage.

As a first step, download the RB-Blitz trial to your prepared drive, and boot the Xbox up into the new user profile you've created.

Go to Settings -> Storage -> USB drive and you should see the RB-Blitz trial showing up, which you can move onto the hard drive. Once moved, you can repurpose the drive as the Bad Update stick.

To prevent accidental Live connections, you can set up the blocking of Live using the Family controls within the settings, but make sure you set content controls to allow running of every rating since the game is `CERO-C (15+)`, so it would get blocked by default settings.

If your Bad Update Stick is done, and RB-Blitz is on your hard drive, just insert the stick into an USB port, unplug your Ethernet cable, then launch RB-Blitz, press A, and when asked to select storage, select the USB storage option.

You should see the `Running exploit...` text on the screen and the ROL on the Xbox changing according to the stage of the procedure. When the chainbreak animation plays, you've successfully ran it!

After the chainbreak animation, you should see a details screen showing your Console Type (such as Trinity, Jasper) and your CPUkey / DVDkey. You can also replug your Ethernet cable when you see this screen. 

To leave this screen, just press the `Back` button (left to the Guide/Xboxlogo button), and it should boot you into Aurora.

(If used BadBuilder), and you're just returned to the normal dashboard, just navigate into the Games screen and you should see an entry named `XexMenu 1.2`, launch it, press left shoulder button until you see the Usb0 storage, and go to Applications > Aurora, and launch `Aurora.xex`.

You should see Aurora booting up. For more details about Aurora, see the [CMods page](https://consolemods.org/wiki/Xbox_360:Aurora).

At this point, if your console has an Ethernet cable plugged in, you should be able to connect to the FTP server launched by Aurora with a program like FileZilla.

If you've already have an extracted folder from PC, you can just send it over FTP to the console to `/Hdd1/Content/USERID/`. To get your `USERID` you can use Aurora's file manager which will show you the names. Also, this is where using the `465607D4` name is preferred.

If the transfer is complete, rescan your library in Aurora, and you should see an entry with the game's name. If you prefer otherwise, you can also use Xex-Menu to launch the game by going to `/Hdd1/Content/USERID/465607D4` and selecting `default.xex`. The game will start.
# Reminder
Don't forget that Bad Update is a non-persistent softmod, so once you shut down the console, you have to relaunch RB-Blitz using the Bad Stick plugged in, or otherwise you can set up [BadAvatar](https://github.com/shutterbug2000/ABadAvatar) to use the Dashboard itself to perform the procedure. However, once you get it done, you can just go ahead and play the game as usual.
