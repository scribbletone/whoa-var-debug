# Debugging Defaults in 4-axis Variable Font

When generating a variable font with fontmake v1.9.1(and 1.9.0), I experience the following weird results in Adobe Illustrator and Photoshop.

- Using the designspace file named `whoa-test.designspace`, everything generates correctly.
- Using the designspace file named `whoa-test-mangled.designspace`, the outlines appear mangled in Photoshop and Illustrator. The only thing that has changed is that the `default` values for each axis are set to an intermediate master, not an extreme.


#### Note
- Only the `H` glyph is included in the example files

#### Expected
![Expected](https://scribbletone.github.io/share/whoa/WHOA-Debug-Expected-1.png)
![Mangled](https://scribbletone.github.io/share/whoa/WHOA-Debug-Mangled-1.png)