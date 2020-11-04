NullDC Emulator README
================
Live documentation here: https://connorcritchley.github.io/proj2/
-----

What is nullDC?

NullDC is an open source Sega Dreamcast and NAOMI emulator for Windows,
developed by drk||Raziel (currently under the nickname skmp) and ZeZu.
It was released under the MIT license.

The emulator was first announced on February 19, 2006, with version
1.0.4 r22 being released May 9, 2010, coinciding with drk||raziel's
discontinuation with the project. 

-----

Requirements and Materials

NullDC requires a machine running Windows 7 or higher, DirectX 9.0c,
Visual C++ runtime libraries and optionally WinPcap for modem emulation.
BIOS files are also needed, and your system may need the files depending
on download source. A controller that is compatible with Windows XInput
system is required.

It has a plugin architecture, with several alternative implementations
(some ported from Chankast) for graphics, sound, reading games burned to
CD-ROMs (it cannot read GD-ROMs directly) or disk image files, memory
cards, etc. Please see those implementation's documentation for uses, as
this will be covering the standard version.

-----

Installation and Setup

1.  Download the emulator (https://www.emuparadise.me/emulators/files/user/NullDC%201.0.4-389.zip)
    
2.  Download any needed BIOS files (https://www.emuparadise.me/biosfiles/bios.html).
    
        The files needed are dc_boot.bin, and dc_flash.bin, and should
        be in the [Dreamcast boot (all regions)] folder at the webpage.

3.  Unzip the nullDC folder and place it where you specify.

4.  Navigate to the data folder.

	If it does not contain dc_boot.bin, and dc_flash.bin, place them inside.

5.  Run nullDC\_Win32\_Release-NoTrace.exe to start the emulator.

6.  Download the games you wish to emulate. One such site to find them
    is (https://www.emuparadise.me/Sega_Dreamcast_ISOs/1). The
    file types that should be downloaded are CDIs.
    
      - It is recommended that you make a separate folder to store these
        CDIs in the same directory as the main nullDC folder, but not
        inside the nullDC folder itself.

7.  Boot up a game.
    
      - Go to the File tab at the top bar of the program, and Select
        Normal Boot.
    
      - In the new window, navigate to the CDI of the game you wish to
        emulate.
    
      - Click OK. The game should begin, with the VMU (Virtual
        Memory Unit, a screen on the original physical controller)
        emulation in a separate window, alongside the separate console
        window.

-----

FAQ

-What gamepads are usable with the emulator?

All versions of nullDC utilize the XInput gamepad framework built by
Microsoft. For the most reliable results, use an Xbox brand controller.


-Is there NetPlay or Online Multiplayer?

There is no such feature implemented, and the additional community
versions past the final release 1.0.4 up to the current 1.0.6 do not
have it either.


-Does it run *every* game for dreamcast?

Unfortunately with the nature of emulators, there are some games that
simply don't work, or suffer graphical or other significant glitches.


-Does this work on Windows 10?

Yes. This version is still confirmed to work as of 10/27/2020. (DRAFT: I
just took the screenshots, so it works for me thankfully)

-----

Troubleshooting

- [File] is missing.

If a message saying that the emulator is missing a file, double check
that DirectX 9 / C++ runtimes are installed and your windows is up to
date.

Common missing files:

  - d3dx9_42.dll - This is a DirectX file.
  - MSVCP100.dll - This is a Windows file.
  - Any file ending in Win32.dll (drkPvr_Win32.dll) followed by a
    Plugin Error [number] - This is a plugin file, it should come
    with the version linked, try re-installing or finding another
    version.


-Controller is not working

Make sure your controller is both supported with XInput, and is
recognized by windows in the device pane.

Ensure your config file has the [hookjoy] section.

Otherwise, you may need to get a separate install of a mapping program
such as Joy2Key.


-Can't run [game]

Some games simply can't be run by the emulator, or will have a
guaranteed crash within it. Search forums or other places to find if
your game is one of them, otherwise check these possibilities:

  - Ensure your CDI files are unzipped.
  - Check that the files were completely downloaded / not corrupted.
  - Some games have more than one disk, in this case have a folder with
    all of the game's CDIs, and choose the folder as the boot file.
  - It might be necessary to find versions of the CDI that are within a
    certain region (USA, Europe should be in parenthesis next to the
    title).


-Immediate crashes / failure to start

Some versions are more volatile than others, with some of the later
community releases being guilty of this. Depending on plugins as well,
some conflicts may occur that lead to crashing.

Try a fresh install of the final official release, 1.0.4.

-----
Support

Unfortunately the project has been dropped, and is no longer officially
maintained. Thankfully, it has been ten years since the end, so there is
a good chance your issue has been encountered before and has been
solved.

But there is still 295 official issues on their page and the last commit
was eight years ago, so some people will just be out of luck.


-----
Licensing

The nullDC emulator was released under the MIT License.


-----
How to Contribute

With the project having been discontinued, there are no further official
updates or means to contribute to one.

However, as the project ended, its creators posted the source code for
others to continue the project on their own. This can be found
at (https://github.com/skmp/nulldc) at their GitHub page.
