# Debugging Defaults in 4-axis Variable Font

When generating a variable font with fontmake v1.9.1(and 1.9.0), I experience the following weird results in Adobe Illustrator and Photoshop. I think I've isolated the issue coming from the `default` values that are used when defining the axes in the designspace file.

- Using the designspace file named `whoa-test.designspace`, everything generates correctly.
- Using the designspace file named `whoa-test-mangled.designspace`, the outlines appear mangled in Photoshop and Illustrator. The only thing that has changed is that the `default` values for each axis are set to an intermediate master, not an extreme.

#### Notes
- Only the `H` glyph is included in the example files
- Both files work fine in Fontview and Chrome. The issue only appears in Adobe applications.
- I've tried with a singled, filled in `H`, and get the same results. In other words no outlined/stroke style, and only one H just following the path of the topmost H. I don't believe it's due to the complexity of the outline. Sorry for not providing this in the example files, but I can do so if that's helpful.
- UFO's are generated from Glyphs.
- Glyphs can generate the variable font, but it seems to mix masters. Moving the scale slider, will instead rotate the glyph sometimes. I think there's a bug in their generation code?

#### Example Images
![Expected](https://scribbletone.github.io/share/whoa/WHOA-Debug-Expected-1.png)
![Mangled](https://scribbletone.github.io/share/whoa/WHOA-Debug-Mangled-1.png)

![Expected](https://scribbletone.github.io/share/whoa/WHOA-Debug-Expected-2.png)
![Mangled](https://scribbletone.github.io/share/whoa/WHOA-Debug-Mangled-2.png)

