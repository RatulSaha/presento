presento
========

A clean, simple and extensible theme for presentations. Supports Xetex and Beamer. 


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


Compulsory packages:
- xcolor (colors)
- fontspec (custom local fonts)
- setspace (line height)
- tikz (shape)
- enumitem (bullet points)

Fonts:
- fontfamilyserif: Montserrat (SIL Open Font License v1.10)
- fontfamilysansserif: Noto Sans (Apache License v2.00)
- fontfamilylight: Lato Light (SIL Open Font License v1.10)

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