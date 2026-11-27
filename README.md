# CJK Fonts for ctex

CJK font files for the ctex `fontset` values `adobe`, `fandol`, `founder` and `windows`, one directory per set, for [TongjiThesis](https://github.com/TJ-CSCCG/TongjiThesis) and other documents built on [ctex](https://github.com/CTeX-org/ctex-kit).

## Font sets

| Directory and `fontset=` | Files | Source | Licence |
| --- | --- | --- | --- |
| `adobe` | `AdobeSongStd-Light.otf`, `AdobeHeitiStd-Regular.otf`, `AdobeKaitiStd-Regular.otf`, `AdobeFangsongStd-Regular.otf` | Bundled with Adobe Reader | Proprietary (Adobe) |
| `fandol` | `FandolSong-Regular.otf`, `FandolSong-Bold.otf`, `FandolHei-Regular.otf`, `FandolHei-Bold.otf`, `FandolKai-Regular.otf`, `FandolFang-Regular.otf` | Fandol team, [CTAN](https://ctan.org/pkg/fandol) (marked obsolete in November 2026) | GPL-3.0 with the font exception |
| `founder` | `FZSSK.TTF` 方正书宋, `FZHTK.TTF` 方正黑体, `FZKTK.TTF` 方正楷体, `FZFSK.TTF` 方正仿宋, `FZXBSK.TTF` 方正小标宋, `FZLSK.TTF` 方正隶书, `FZXH1K.TTF` 方正细黑一, `FZY1K.TTF` 方正细圆, `FZY3K.TTF` 方正准圆 | Bundled with WPS Office | Proprietary (Founder); 书宋, 黑体, 楷体 and 仿宋 are free for publishing use ([Founder](https://www.foundertype.com/index.php/About/powerbus.html)) |
| `windows` | `simsun.ttc` 宋体, `simhei.ttf` 黑体, `simkai.ttf` 楷体, `simfang.ttf` 仿宋, `simli.ttf` 隶书, `simyou.ttf` 幼圆, `msyh.ttc` and `msyhbd.ttc` 微软雅黑 | Bundled with Microsoft Windows | Proprietary (Zhongyi Electronic, Microsoft) |

## Download

Each [release](https://github.com/TJ-CSCCG/cjk-fonts-for-ctex/releases) carries one zip per set. The latest is always at:

```text
https://github.com/TJ-CSCCG/cjk-fonts-for-ctex/releases/latest/download/<set>.zip
```

where `<set>` is `adobe`, `fandol`, `founder` or `windows`. Download from releases rather than from the repository files: the files are stored with Git LFS, whose bandwidth is limited, while release downloads are not.

## Usage

- **TongjiThesis:** run `make fonts` (Windows: `.\make.bat fonts`) to download the `windows` set into the project's `fonts/` folder, where the class finds it. On Overleaf, upload the files from the zip into a `fonts/` folder in the project. See the TongjiThesis README for the other sets.
- **Other ctex documents:** install the fonts in your system font directory, refresh the font cache (`fc-cache -fv` on Linux), then compile with the matching `fontset=`:

  ```latex
  \documentclass[fontset=windows]{ctexbook}
  ```

## Releases

Releases are cut by [release-please](https://github.com/googleapis/release-please) from Conventional Commits on `main`: merging its release pull request creates the tag and the release, and the workflow attaches the zips.

## Disclaimer

This repository provides font files **for educational and academic reference only**. The fonts are not authored or owned by this project:

- **Fandol** fonts are licensed under the GPL-3.0 with the font exception, and may be redistributed under its terms.
- **Adobe**, **Microsoft (SimSun, SimHei and the others)** and **Founder (方正)** fonts are proprietary typefaces owned by their copyright holders. They are provided only to help students typeset theses in the typefaces their institutions require. They are not licensed for commercial use, redistribution, or embedding in published works without authorization from the copyright holders.

Users are responsible for complying with the font licences that apply to them.

## See also

- [ctex-kit](https://github.com/CTeX-org/ctex-kit): the ctex macro package
- [TongjiThesis](https://github.com/TJ-CSCCG/TongjiThesis): the Tongji University undergraduate thesis template
- [notofonts/noto-cjk](https://github.com/notofonts/noto-cjk): Noto CJK, free, full Unicode coverage
