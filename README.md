# icanfont
My iconfont development workflow!

## Making iconfonts with SVGs is now a whole lot easier
Making iconfonts using a set of SVGs used to be annoying because every svg to ttf converter I've seen would ignore the strokes in SVG and give a neat result only if the glyph was bounded by paths. I've automated the process using inkscape cli and a shell script that i wrote (stroketopath.sh). Here is a sample workflow of the whole thing. Feel free to clone it and use it for your projects. 

See below for usage instructions

## Prerequisites

1. Inkscape is installed and CLI is available on the terminal
2. Node and npm are installed 
3. Node package [glyphs2font](https://github.com/rse/glyphs2font) is installed globally.

You can check for these as follows:
```
$ inkscape -V
Inkscape 0.92.3 (2405546, 2018-03-11)

$ node -v
v8.11.3

$ npm -v
6.1.0

$ glyphs2font
glyphs2font: ERROR: invalid number of arguments
glyphs2font: USAGE: glyphs2fonts <yaml-config-file>
```

## Usage
1. Place your SVG glyphs in the 'glyphs' folder
2. Map unicode characters to SVG glyphs and change other settings in settings.yml. Refer to [glyphs2font/README.md](https://github.com/rse/glyphs2font) for full specification
3. Run makefont.sh
4. See output in 'font'

## Acknowledgements
* [rse](https://github.com/rse) for [glyphs2font](https://github.com/rse/glyphs2font)
