# Library Quote Yanti

Homepage lettering: 「積學以儲寶，酌理以富才。」

This font is a subset of **I.Ngaan / 刻石錄 I.顏體 1.004**, released under
**GNU GPL version 2 or any later version**, as stated in the original font's
copyright and license metadata. See `LICENSE.txt` for the GPL version 2 text.

Original copyright:

- (C) Dr. Hann-Tzong Wang, 1999–2004.
- (C) Ichiten Fonts Project, 2013–14.

Author page: https://founder.acgvlyric.org/iu/doku.php/造字:開源字型_i.顏體

Download mirror: https://github.com/wordshub/free-font/blob/master/assets/font/中文/刻石录系列/I.顏體.ttf

Original TTF SHA-256:
`7aba8f5bb77ea7e0fc37c0e5e709bd8e1d49b44a3c91eb503f426562602f9c2a`

## Modifications and source

Modified for Linguista Library on 2026-09-23: keep only the 11 distinct characters
in the quote; rename the family to `Library Quote Yanti`; compress as WOFF2.
The glyph outlines are unchanged. This modified font remains GPL-2.0-or-later.

`library-quote-yanti.ttf` is the editable TrueType source corresponding to the
WOFF2 delivered by the homepage. The original copyright and license metadata
are retained in both files. No warranty is provided.

The repository's `scripts/subset-library-yanti.py` reproduces both files from
the original font, checks its SHA-256, and verifies character coverage. Run in
the `henri_env` environment with fontTools and Brotli:

```sh
python scripts/subset-library-yanti.py /path/to/I.Ngaan.ttf
```

The homepage WOFF2 can also be reproduced directly from the supplied editable
TTF with fontTools:

```python
from fontTools.ttLib import TTFont
font = TTFont("library-quote-yanti.ttf", recalcTimestamp=False)
font.flavor = "woff2"
font.save("library-quote-yanti.woff2")
```

The subset covers only this quote. Changing its characters requires rebuilding
the subset and updating the `unicode-range` in `src/pages/index.astro`.
