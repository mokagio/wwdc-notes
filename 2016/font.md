# [Typography and Fonts](https://developer.apple.com/videos/play/wwdc2016/803/)

## Terminology

**Text** encodes language and convenes meaning.

Text is made of **characters**.

A character is an _abstract unit of text_ and it is represented by a code, i.e.:

```
A = U+0041
```

Characters are defined by the Unicode consortium.

The visual representation of a character is called **glyph**.

Glyph are stored in a file called **font**.

There is not a 1:1 mapping between characters and glyphs, there are
**typographic features** that, for example, combine two characters into one (ligature).

Fonts can have different **styles**: bold, italic, condensed, etc.

All the styles are tide together by a typefaces, the _design DNA_ of a font, the idea of a set of shapes.

**Typography** is the act of using type and typefaces to set text and encode language.

**Spacing**: the empty space around a glyph, it's built into the font, and the type designers configured it to have an even distribution of the text.

**Tracking**: a property that allows to modify the space in between one glyph and the other, at a global level.

**Kerning**: exception mechanism to change the spacing between a specific pair of glyphs. All the information is stored inside the font in the kerning table, and as such we cannot change it.

**Leading**: space between the lines, we can control it.

## Recap

![](https://dl.dropboxusercontent.com/u/3085551/wwdc-2016-typograhy-and-fonts-terminology.png)

Text is made up by characters. Characters are represented by glyphs. The
relationship between characters and glyphs can be altered/controlled by
typographic feature. Glyphs and features are stored in a font file, which can
have multiple styles. All the styles are group under a typeface umbrella, which
is the idea behind the design of the font. Finally, typography is the use of
all this to convey text.

## Legibility

_Continue from 11:08_
