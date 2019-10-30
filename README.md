# X16-dev

## Development of X16 Software by Simon Jackson

This is a repository for maintaining version control.
Things will be copied across as an when necessary to
facilitate my sanity of distraction from version updates. It's growing all the time. The following library files are active.

* *baselib.mfk* - Mainly graphics configuration and base initialization and shutdown functions.
* *input.mfk* - An input library for joypad and "disk".
* *main.mfk* - The main file for the current build.

New files will be added and renamed as and when the code matures for any particular thing. The code generator for *Millfork* is quite good as it seems to not make code which is not reached. Language perculiarities are few, but there non the less.

As the scale of single *.prj* files is not too large, it does not seems that necessary to version control updates with releases. The repository master branch will be "tagged" when something suitably new is added. This will generally be before extream edits to the *main.prj* and *main.mfk* files with the older versions backed up as *[title].mfk* and *[title].mfk*, with possible extra resources added named *[title].bmp* for example.

## Palette and Glyph Resources

A glyph *.xcf* file for a 256 colour export as a *.bmp* file (uncompressed) and this will be later imported. The top left corner contains invariant palette information and a logo space. the the small font in two half image blocks, along with the large font. Then the three directions of the tile big glyphs follow. The palette was placed first for dynamic loading, although the palette data follows pixel data, and so can be automatically processed. Finally the *.bmp* palette data can be processed to automatically fill the palette registers.

There are no plans for editing and saving the file on the X16 as emulator screen capture and paste in gimp is quite good. The palette is in 16 colour blocks for 4 bpp processing while keeping the edit coloured right. The loader could eventually support 8 bpp when the best format is decided. With map grids minus the palette corner at 4 bpp the *.bmp* takes up all 128 kB of the VRAM. The big glyphs are for display on layer 0, with an overlay of text in small glyphs on layer 1. Layer 0 will form a complete 512 by 448 bitmap at 4 bpp, which can be drawn onto or mapped to rearrange. The pixel order will be different than regular bitmap mode.

It is yet to be observed if PLL bit clock modification can stretch the bitmap to fill the screen. In the emulator this maybe more possible than on real hardware. By default the border and all 224 small glyphs making an 8 pixel scroll border might not be suitable for all purposes. The trade off of more colours using 4 bpp instead of 2 bpp is considered by me to be worth a border around the play area for nicer colour experience.

## (TBC)

The below have yet to be decided.

## Logo Resource

This is a small logo to be done at 32 by 16 in 4 bpp. Just because it can be so. It also makes for a complete filling of the graphics memory at the chosen resolution for my first project demo.

## Tiny AI

This will be a simple AI to test out some optimization ideas, and some other generic categorization of the processes of simulation of being. It may include a little bit of genetic algorithms, neural nets on a mini scale, and some optimization ideas on PID motion control. The 8-bit target limits the functionality, but presents some interesting optimization challenges.

## Some Format Conversion Resources

This will be a set of portable tools for turning the resource files into loadable images and sounds. It should be quite automatable for a good production pipeline for easy edit to release cycling.

## A Demo Game

A nice game utilizing the resources provided here. The full story has not been decided. The tools I make will be open source and usable by other people for commercial release, so long as the game graphics, sound, story and strategy differ sufficiently for it to be another interesting game and not just another clone.

## On Device Editors

The end aim is development of some on device utilities to edit, load and save all the resources that will be provided. This will make the conversion tools a bootstrap process.
