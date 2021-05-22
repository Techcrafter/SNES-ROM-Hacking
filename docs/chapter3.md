![The SNES ROM hacking guide](https://raw.githubusercontent.com/Techcrafter/SNES-ROM-Hacking/main/docs/images/banner.png)

# Chapter 3: Regions And Headers

## Different Regions

It is pretty obvious that Nintendo released different console models for different regions. Those regions are the following:

|Region Code|Region       |Video Format|Console name                       |
|-----------|-------------|------------|-----------------------------------|
|J          |Japan        |NTSC        |Super Famicom                      |
|U          |United States|NTSC        |Super Nintendo Entertainment System|
|E          |Europe       |PAL         |Super Nintendo Entertainment System|

The main reason for this decision was to feature the different video formats for the different regions.
Another, maybe not so obvious reason for this decision, was to prevent some Chinese and Japanese "manufacturers" to pirate games too fast. This is called a **region lock**. This causes a game from Japan not to work in a European console.

![A Super NES from the United States](https://c4.wallpaperflare.com/wallpaper/388/1016/1009/computer-game-console-device-electronics-wallpaper-preview.jpg) ![A Super NES from Europe](https://c4.wallpaperflare.com/wallpaper/74/954/404/snes-wallpaper-preview.jpg)

*A Super NES from the United States / A Super NES from Europe*

As you can see on the pictures above, even the designs of the consoles were very different!

But this is not all about the different regions. Some games like "A Link To The Past" or "Secret of Mana" were even translated into single languages. This happened because reading text is actually really important in those games, so they translated those in multiple languages.

![A screenshot from the German version of ALTTP](https://raw.githubusercontent.com/Techcrafter/SNES-ROM-Hacking/main/docs/images/german-alttp.png)

*A screenshot from the German version of ALTTP*

[Here is a list with the different codes and their meaning](https://www.emuparadise.me/help/romnames.php).

## Headers

Each official Nintendo ROM has a header. The header is important for the console because it contains information like cartridge/ROM size, additional chips (Super FX, SA-1, ...), if the game has a SRAM and more.

**The header is only important for consoles! Most emulators will run ROM files without a header as well.**

## Effects on patching ROM files

When patching a ROM it is important to check what for a ROM you need to patch!
A ROM hack for a United States ROM will (in most cases) not work with a Japanese ROM for example.
This depends on how similar both versions of the games are, but in most cases it will not work.

It is also important to check if you need a ROM with or without header.

Here's an example filename:
Super Mario World (J) [!].smc

  * "Super Mario World" is the name of the game.
  * "(J)" means that you need the Japanese version of the game.
  * "[!]" simply means that you need should use an error free dump.
  * ".smc" is the file extension. ".sfc" would work as well!

### Removing and adding a header

The header of a game can be easily removed and added:

  * Make sure that the write protection for the ROM file is not enabled (right click on the file > Properties).
  * Open SNEStuff and click on "Add or remove header".
  * Select your ROM.
  * SNEStuff automatically adds or removes the header from the ROM you have selected!

![SNEStuff automatically adds or removes the header](https://raw.githubusercontent.com/Techcrafter/SNES-ROM-Hacking/main/docs/images/add-remove-header.png)

*SNEStuff automatically adds or removes the header*