DCG tGIF Maker
================================

## Description

**_DCG tGIF Maker_** generates transparent GIF file of DCG(Destiny Child game)'s character. 

It's *viewer* (https://DCG-tGIF.github.io/) extracts transparent PNG files of DCG(Destiny Child game)'s character frame by frame.
And using *apngasm_gui/apng2gif_gui* contained on it, you can make animated image file as you want.

 - 한국어 설명은 README_Korean.md 에서 볼 수 있습니다.


## References

This tool is made by modifying some source codes of viewer site [Live2D-DCG.github.io](https://live2d-dcg.github.io/) (https://github.com/Live2D-DCG/Live2D-DCG.github.io).

[apngasm](http://apngasm.sourceforge.net/), [apng2gif](http://apng2gif.sourceforge.net/) tools can download for each sites, and also they are included in this tool.

[JSZip](https://stuk.github.io/jszip/) is used to compress images on the browser to be downloaded at once.


## Usage

This is the process how to make animated GIF.

    1. Change the character and canvas settings using reload, and get images you want.
    2. Make animated PNG file using apngasm_gui.
    3. Make animated GIF file using apng2gif_gui.

In a similar way, you can also make webp file using online converter site.


## Apply Custom Texture Images

This is the process how to load custom texture images on the character.

    1. Rename texture image file to texture_00.png
      1-1. if there exists two images, rename texture_00.png and texture_01.png in order.
    2. Click custom texture choice button and choose texture files.
