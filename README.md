presento
========

Presento is a clean, simple and extensible template for presentations — supported by XeTeX and Beamer. XeTeX is a TeX typesetting engine that can be [thought](http://tex.stackexchange.com/questions/3393/what-is-xetex-exactly-and-why-should-i-use-it) of as standard LaTeX (pdftex) with support for Open Type Fonts. Beamer is a widely used LaTeX class for presentations and slides.

## Demo

* [Minimal demo](http://www.comp.nus.edu.sg/~ratul/public/presento.pdf) (PDF)
* A group [presentation](http://www.comp.nus.edu.sg/~ratul/public/BoS_final_presentation.pdf) (PDF) for a business class

## Installation

For novice TeX users, it is highly recommended to use [shareLaTeX](http://www.sharelatex.com/), a fascinating online TeX editor. The installation is as simple as downloading presento and uploading to shareLaTeX as a new project.

To use presento in your local computer, install XeTeX and the compulsory packages listed below. These mostly come as part of the popular TeX engines like [MiKTeX](http://miktex.org/).

Compulsory packages:
* `xcolor` (used for adding colors)
* `fontspec` (supports for custom local fonts)
* `setspace` (handles the spacing between lines)
* `tikz` (used to draw for various shapes)
* `enumitem` (custom lists)

## Fonts

The primary fonts in use are [Montserrat](http://montserrat.zkysky.com.ar/en) by Julieta Ulanovsky, [Lato](http://www.latofonts.com/) (Light) by Łukasz Dziedzic and [Noto](https://www.google.com/get/noto) Sans by Google. For small caps, [Algreya Sans](http://www.huertatipografica.com/fonts/alegreya-sans-ht) (small caps variation) by Juan Pablo del Peral is used. [Inconsolata](http://en.wikipedia.org/wiki/Inconsolata) by Raph Levien is used as a monospaced font.

Except Noto Sans, which is licensed under Apache License v2.00, all other fonts used are under SIL Open Font License v1.10. In short, all the fonts are free to use and redistribute under the terms of the respective licenses. 

The fonts and their usage are already baked into the template. However for custom use, the following LaTeX commands (without any arguments) are provided: `\montserratfont`, `\notosansfont`, `\latolightfont`,`\inconsolatafont`.

## Colors

The color palette is vibrant, bold yet minimal. The following colors can be used with the `\color{colorName}` command.

* `colorlgray`: #FAFAFA (light gray)
* `colordgray`: #795548 (dark gray)
* `colorhgray`: #212121 (heavy dark gray)
* `colororange`: #E65100 (orange)
* `colorgreen`: #009688 (green)
* `colorblue`: #0277BB (blue)

## Custom Macros

* `\hugetext{text}`: sets the huge, bold text. It should only be used for short and bold statements.
* `\largetext{text}`: sets a large text. It should be used as subheadings, lines with less than 40 characters.
* `\setnote{text}`: sets a smaller text with color gray. It should be used for showing notes such as url, references etc.
* `\framecard[optionalColor]{mainText}` - Sets the big bold mainText at center with a background color of optionalColor, which is colorgreen by default. It should be used for flashing ideas, introducing subsections etc.
* `\framepic[optionalOpacity]{image}{content}` - Sets the image as a background of the full frame with opacity set to optionalOpacity. The frame may have content inside.

## Custom environments

* `\begin{baseitemize} \end{baseitemize}`: This is standard itemize without any indentation. It should be used for normal listing.
* `\begin{fullpageitemize} \end{fullpageitemize}`: This is used for listing in full frame. The items in the list are  properly spaced. It should be used for listing points in one full frame.

## Concluding remarks

The typography and design principles have been largly influenced by notable designers around the world. Sincere thanks goes to [Prof. Dr.-Ing. André Miede](http://www.miede.de/) (developer of [Classicthesis](https://code.google.com/p/classicthesis/)), Robert Bringhurst (author of 'The Elements of Typographic Style'), Richard Rutter (creator of The Elements of Typographic Style Applied to the Web), Tim Brown (developer of [Modular Scale](http://modularscale.com)), designers at [Google](https://google.com/design) among others.

This work is not licensed. Feel free to use, modify, redistribute. Comments and suggestions are welcome!

## FAQ

#### While using `\framepic`, why is the image not shown in full screen?

Please check the image size and aspect ratio. While not obligatory for any rules, you may want to note that the standard beamer template size is 12.8cm x 9.6cm.

#### How do I change the font sizes?
The spacing and font sizes are carefully designed. Change font sizes by using `\fontsize{size}{leading}\selectfont` only if you are sure of what you are doing.

#### Why does the text in my presentation look pale?
High contrast of black-white is not advisable for presenting with high quality projectors. Thus the background is set to light gray and the text color is set to heavy dark gray. If you are unsure about the quality of the projector and/or the text looks pale, comment out the following in config/presento-config.tex:
```
\setbeamercolor{background canvas}{bg=colorlgray}
\setbeamercolor{normal text}{fg=colorhgray}
```