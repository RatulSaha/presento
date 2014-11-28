presento
========

Presento is a clean, simple and extensible theme for presentations - supported by XeTeX and Beamer. XeTeX is a TeX typesetting engine that can be [thought](http://tex.stackexchange.com/questions/3393/what-is-xetex-exactly-and-why-should-i-use-it) of as standard LaTeX (pdftex) with support for Open Type Fonts. Beamer is a widely used LaTeX class for presentations and slides.

## Installation

For novice TeX users, it is highly recommended to use [shareLaTeX](http://www.sharelatex.com/), a fascinating online TeX editor. The installation is as simple as downloading presento and uploading to shareLaTeX as a new project.

To use in your local computer, install XeTeX and the compulsory packages listed below. These mostly come as part of the popular TeX engines like [MiKTeX](http://miktex.org/).

Compulsory packages:
* `xcolor` (used for adding colors)
* `fontspec` (supports for custom local fonts)
* `setspace` (handles the spacing between lines)
* `tikz` (used to draw for various shapes)
* `enumitem` (custom lists)

# Fonts

The primary fonts in use are Montserrat, Lato (Light) and Noto Sans. For small caps, Algreya Sans (small caps variation) is used. Inconsolata is used as a monospaced font.

Except Noto Sans, which is licensed under Apache License v2.00, all other fonts used are under SIL Open Font License v1.10. In short, all the fonts are free to use and redistribute under the terms of the respective licenses. 

The usage of the fonts are already baked into the template. However, for custom use, the following custom LaTeX commands (without any arguments) are provided: `\montserratfont, \notosansfont, \latolightfont,\inconsolatafont`.


Useful Macros:

- \hugetext{text}: sets the large, bold text. To be used for large and bold statements only.
- \largetext{text}: sets a little larger text. To be used as subheadings in boy (not the title of the frame)
- \setnote{text}: sets a smaller text with gray color. Can be used for showing notes such as url, references etc.
- \framecard[optionalColor]{mainText} - Sets a big bold text at center with a background color, which is colorgreen by default.

Custom environments:
- baseitemize: Replacement of itemize without any indentation
- fullpageitemize: use for full page, properly spaced list of items in a page

Note to self:
- Typography
- Only em is used.
- Modular typography?
- Beamer template size: 12.8cm x 9.6cm
- % Prefer to choose among {0.541, 0.618, 0.875, 1.417, 1.618, 2.292, 2.618, 3.708}, though not strict
- comment out the following in config/presento.sty if the projector is not of high quality and the text looks pale
   \setbeamercolor{background canvas}{bg=colorlgray}
   \setbeamercolor{normal text}{fg=colorhgray}


Colors:
- colorlgray: #FAFAFA % background light gray
- colordgray: #795548 % dark gray for notes
- colorhgray: #212121 % heavy dark gray for normal text (optional)
- colororange: #E65100 % orange
- colorgreen: #009688 % green
- colorblue: #0277BB % blue


Thanks to:
- .gitignore-latex (https://gist.github.com/misberner/8316891)
- Classicthesis (https://code.google.com/p/classicthesis/)
- Tim Brown (http://modularscale.com)
- Google Design (https://google.com/design)