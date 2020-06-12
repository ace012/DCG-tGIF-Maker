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

This is the process how to make GIF file on local.

    1. Change the character canvas using reload, and get images (HQLS recommended). This process needs a few minutes.
    2. Make animated PNG file using apngasm_gui.
    3. Make animated GIF file using apng2gif_gui.


## Additional

On the viewer site, there are Korean pck files only.

But you can also extract images of other pck files, such as global (or teen) version, or custom pck files.

I plan to add that more easy and comfortable version later, but I don't know when it will be.

If you want to get ones right now, you can extract it as following this below.


### Caution

If you will run viewer of this tool on web server, there is no problem.

But if you just run viewer locally(maybe most of them), you should bypass one of the security policy, *CORS(Cross-Origin Resource Sharing)*.

Thus, It is recommended to use other browser than using one now, and you must not enter any websites on that browser.

You can bypass CORS in local html by adding "--allow-file-access-from-files" argument on shortcut of browser.

This is the detail progress.

    1. Make a shortcut of your browser used for viewer.
    2. Right click the shortcut and press properties.
    3. Add "--allow-file-access-from-files" text on the end of the Target Textbox.
    4. Execute shortcut.


### Usage

This is the process how to make GIF file on local.

    1. Open browser using shortcut.
    1-1. Press F12 to open developer window. On the Network tab, switch online to offline.
    2. Drag & Drop viewerK.html on browser.
    3. Change the character canvas using reload, and get images (HQLS recommended). This process needs a few minutes.
    4. Make animated PNG file using apngasm_gui.
    5. Make animated GIF file using apng2gif_gui.

And this is the method to add child unpack file.

1. Download .exe file on https://github.com/Live2D-DCG/DCG which is appropriate file for your pck file.
2. Drag & Drop your PCK file to .exe file downloaded.
3. Move the result folder to DCGViewer\static\Korean.

