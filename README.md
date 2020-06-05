DCG tGIF Maker
================================

## Description

**_DCG tGIF Maker_** generates transparent GIF file of DCG(Destiny Child game)'s character. 

It's *viewerK.html* extracts transparent PNG files of DCG(Destiny Child game)'s character frame by frame.
And using *apngasm_gui/apng2gif_gui* contained on it, you can make animated image file as you want.

 - 한국어 설명은 README_Korean.md 에서 볼 수 있습니다.


## References

This tool is made by modifying some source codes of viewer site [Live2D-DCG.github.io](https://live2d-dcg.github.io/) (https://github.com/Live2D-DCG/Live2D-DCG.github.io).

Also, [JSZip](https://stuk.github.io/jszip/) is used to compress images on the browser to be downloaded at once.


## Requirements

There are several requirements for using this tool.

    1. Chromium browser (or Chrome)
    2. PNGs to APNG tool (apngasm)
    3. APNG to GIF tool (apng2gif)
    4. Unpacked child file

The materials 1~3 are included here.


## Caution

If you will run viewer of this tool on web server, there is no problem.

But if you just run viewer locally(maybe most of them), you should bypass one of the security policy, *CORS(Cross-Origin Resource Sharing)*.

Thus, It is recommended to use other browser than using one now, and you must not enter any websites on that browser.

You can bypass CORS in local html by adding "--allow-file-access-from-files" argument on shortcut of browser.

This is the detail progress.

    1. Make a shortcut of GoogleChromePortable64/GoogleChromePortable.exe (or your browser used for viewer).
    2. Right click the shortcut and press properties.
    3. Add "--allow-file-access-from-files" text on the end of the Target Textbox.
    4. Execute shortcut.


## Usage

This is the process how to make GIF file on local.

    1. Open browser using shortcut.
    1-1. Press F12 to open developer window. On the Network tab, switch online to offline.
    2. Drag & Drop viewerK.html on browser.
    3. Change the character canvas using reload, and get images (HQLS recommended). This process needs a few minutes.
    4. Make animated PNG file using apngasm_gui.
    5. Make animated GIF file using apng2gif_gui.

There is no child unpack file here.
You should add unpack file on DCGViewer\static\Korean, or download from https://github.com/Live2D-DCG/Live2D-DCG.github.io .

And this is the method to add child unpack file.

1. Copy child unpack file you want on DCGViewer\static\Korean.
2. Change file names according to the condition. (Reference script: https://github.com/Live2D-DCG/DCG/blob/master/Live2D%20Scripts)

if there are 3 txt files,

    00000000.txt -> [dir_name]_attack.mtn
    00000001.txt -> [dir_name]_hit.mtn
    00000002.txt -> [dir_name]_idle.mtn
    00000003.moc -> character.dat
    00000004.dat -> MOC.[dir_name].json

or if there are 4 txt files,

    00000000.txt -> [dir_name]_attack.mtn
    00000001.txt -> [dir_name]_banner.mtn
    00000002.txt -> [dir_name]_hit.mtn
    00000003.txt -> [dir_name]_idle.mtn
    00000004.moc -> character.dat
    00000005.dat -> MOC.[dir_name].json

And, all of the png files should change texture_00.png, texture_01.png, ... as in order.

if the file is spa character file,

    00000000.moc -> character.dat
    00000001.dat -> MOC.[dir_name].json
    00000002.physics -> physics.json
    00000003.txt -> [dir_name]_idle.mtn
    00000004.txt -> [dir_name]_max.mtn
    00000005.txt -> [dir_name]_maxtouch.mtn
    00000006.txt -> [dir_name]_touch.mtn

Also, all of the png files should change texture_00.png, texture_01.png, ... as in order.
