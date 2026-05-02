# CJK Fonts for ctex

CJK font files referenced by [ctex](https://github.com/CTeX-org/ctex-kit) fontset definitions. Organized by `fontset` value for use with `\documentclass[fontset=...]{ctexbook}` or [TongjiThesis](https://github.com/TJ-CSCCG/TongjiThesis).

## Fontsets

| Directory  | `fontset=` | Fonts                                                                 | Source                         |
| ---------- | ---------- | --------------------------------------------------------------------- | ------------------------------ |
| `adobe/`   | `adobe`    | Adobe Song / Heiti / Kaiti / Fangsong Std                             | Bundled with Adobe products    |
| `fandol/`  | `fandol`   | Fandol Song / Hei / Fang / Kai                                        | TeX Live (SIL OFL)             |
| `founder/` | `founder`  | Founder 书宋 / 黑体 / 楷体 / 仿宋 / 隶书 / 幼圆 / 小标宋 / 细黑一     | Bundled with WPS Office        |
| `windows/` | `windows`  | SimSun / SimHei / SimKai / SimFang / SimLi / SimYou / Microsoft YaHei | Bundled with Microsoft Windows |

## Usage

```latex
% Pick one of the fontsets provided in this repository:
\documentclass[fontset=fandol]{ctexbook}   % cross-platform, ships with TeX Live
\documentclass[fontset=windows]{ctexbook}  % requires SimSun/SimHei/…
\documentclass[fontset=adobe]{ctexbook}    % requires Adobe CJK fonts
\documentclass[fontset=founder]{ctexbook}  % requires Founder fonts
```

Install fonts to your system font directory, refresh the font cache (`fc-cache -fv` on Linux/macOS), then compile as usual.

## Disclaimer

This repository provides font files **for educational and academic reference only**. The fonts are NOT authored or owned by this project:

- **Fandol** fonts are released under the [SIL Open Font License 1.1](https://openfontlicense.org/) and are freely redistributable.
- **Adobe**, **Microsoft (SimSun/SimHei/…),** and **Founder (方正)** fonts are proprietary typefaces owned by their respective copyright holders. These files are provided solely to assist students in typesetting academic theses with the correct typefaces required by their institutions. They are NOT licensed for commercial use, redistribution, or embedding in published works without proper authorization from the copyright holders.

Users are responsible for ensuring compliance with applicable font licenses in their jurisdiction.

## See Also

- [ctex-kit](https://github.com/CTeX-org/ctex-kit) — ctex macro package
- [TongjiThesis](https://github.com/TJ-CSCCG/TongjiThesis) — Tongji University undergraduate thesis template
- [notofonts/noto-cjk](https://github.com/notofonts/noto-cjk) — Noto CJK (free, full Unicode coverage)
