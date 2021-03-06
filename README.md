# Micro-GUI (ugui)

Micro-GUI (ugui) is a minimal GUI framework for embedded systems, because there seems to be a lack of open source embedded gui tools, and we should share more.

Heavily inspired by the [Pebble](https://getpebble.com) User Interface API (which is seriously great, and you can check out [here](https://developer.getpebble.com/docs/c/User_Interface/)).

It provides a simple window stack, layers for composition of windows, graphics functions for rendering primitives and text, and widgets to simplify commonly used functions.

If you have any issues or feature requests, feel free to open an issue or a pull request. And, if you find yourself using this in a project, I would love to know about it!

## Alternatives
 - [u8glib](https://github.com/olikraus/u8glib) A graphics library with support for many different displays.
 - [m2tklib](https://github.com/olikraus/m2tklib) Mini Interative Interface Toolkit Library. A portable graphical and character user interface (GUI+CUI) library for embedded systems
 - [UGUI](https://github.com/achimdoebler/UGUI) A free and open source graphic library for embedded systems
 - [ttf2ugui](https://github.com/AriZuu/ttf2ugui) A free and open source ttf to font array converter for UGUI above

## Build Status
[![Build Status](https://travis-ci.org/ryankurte/micro-gui.svg)](https://travis-ci.org/ryankurte/micro-gui)

## Goals
 - Simple to embed
   - No (or minor) external dependencies
   - Permissive licensing (MIT)
   - C compliant, doesn't force the use of c++
 - Simple to use
   - Minimal API
   - Widgets for common functions
   - Examples for all components
   - API documentation?
 - Simple to develop
   - Object Oriented C
   - Clearly defined modules
 - Simple to test
   - Compiles for any platform (bmp export requires file.h)

## Status

 - Window stack / top level interface working
 - Layers mostly working
 - Graphics module 
   - layer offsets implemented, need to implement bounds
   - text rendering implemented
 - Asset pipeline
   - OpenIconic - generation complete, needs functions to convert to sprites
   - Fonts - complete, converts .ttf fonts to directly compatible c source/header files
 - Widgets
   - working on menu
   - todo: progress bar, alert/message box, buttons
 - Testing, needs to be implemented (w/ CI)
 - Example, work in progress using SDL2

## Getting Started

 - Checkout project with `git clone git@github.com:ryankurte/micro-gui.git`
 - Create build directory with `mkdir build`
 - Change to build directory with `cd build`
 - Initialize cmake with `cmake ..`
 - Build with `make`
 - Run with `./ugui`

## Examples

For an example application see the `example/` folder. This application will update a bmp file each rendering call, and can be interacted with using the command line.

## Credits

 - [Pebble](https://getpebble.com) for inspiration 
 - Line and Ellipse functions adapted from [here](https://www.opengl.org/discussion_boards/showthread.php/168761-Drawing-Line-Bresenhem-midpoint-algorithm)
 - Fonts from [here](https://github.com/dhepper/font8x8)

## License

This project is experimentally licensed under the terms of the MIT license, because LGPL even with a static linker exception requires you to provide tools to relink your application against the library, which in my opinion is too greater barrier to usage/adoption.

As such, if you make improvements to this library, it would be awesome if you would contribute them back. If that doesn't work, well, we will have to switch to something like the LGPL.

See LICENSE.TXT for more information

