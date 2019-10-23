# X16-dev
## Development of X16 Software by Simon Jackson
This is a repository for maintaining version control.
Things will be copied across as an when necessary to
facilitate my sanity of distraction.

# (TBC)

## Palette and Glyph Resources
A .txt file palette and a glyph .xcf file for a 256 colour export
so that later a 16 colour export is possible. Bottom two lines should have palette rows, so that the colour is not remapped by tools, and palette assignment can be automated.

## Font Resources
I think the font resources should be built from the glyph resources if necessary, but I may decide otherwise. There are more small font glyphs for example, and so some need defining.

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