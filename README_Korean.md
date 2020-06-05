Live2D Transparent Image Crawler
================================

## Description

본 툴은 데스티니 차일드 캐릭터의 투명 배경 이미지 파일을 프레임 단위의 PNG 파일로 추출할 수 있습니다. 이를 통해 원하는 차일드의 투명 배경 움짤을 만들 수 있습니다.

이 툴은 데스티니 차일드 캐릭터 Live2D 뷰어 사이트인 Live2D-DCG.github.io (https://github.com/Live2D-DCG/Live2D-DCG.github.io) 사이트를 수정하여 만들어졌습니다.
또한, 브라우저에서 이미지들을 압축하여 한번에 다운로드받을 수 있도록 하기 위해 JSZip (https://stuk.github.io/jszip/) 를 차용하였습니다.



## Requirements

본 툴을 사용하기 위해서는 몇 가지 준비물이 필요합니다.

1. Chrome 브라우저 (또는 Chromium)
2. PNGs to APNG tool (apngasm)
3. APNG to GIF tool (apng2gif)
4. 언팩된 차일드 파일

1~3의 준비물은 본 툴과 함께 동봉되어 있습니다.



## Caution

본 툴은 브라우저의 보안 정책 중 하나인 CORS를 우회해야만 동작합니다.
그렇기 때문에 가급적이면 쓰지 않는 브라우저를 따로 사용하는 것을 권장하며, 해당 브라우저로는 다른 웹사이트에 접속하지 않도록 합니다.
이 툴에는 쓰기 적합한 크롬 포터블 버전(GoogleChromePortable64.zip)을 동봉하였습니다.

결론은 chrome(또는 chromium)에 --allow-file-access-from-files 를 인자로 줘서 로컬에서 CORS를 우회하여 사용할 수 있도록 해주어야 합니다.
자세한 설명은 Manual의 browser을 읽어보시면 되겠습니다.

인자를 주는 방법은 아래와 같습니다.

1. GoogleChromePortable64/GoogleChromePortable.exe (또는 사용할 브라우저)를 우클릭하여 바로가기를 만듭니다.
2. 만들어진 바로가기를 우클릭하여 속성을 누릅니다.
3. 대상의 텍스트 맨 뒤쪽 exe 뒤에 --allow-file-access-from-files 를 추가합니다.
4. 이후 "이 바로가기를 통해서 브라우저를 실행할때만" 해당 인자를 준 채로 실행하게 됩니다.



## Usage

아래는 움짤을 만드는 방법입니다.

1. 위에서 만든 바로가기를 이용하여 브라우저를 켭니다.
1-1. F12를 눌러 개발자 창을 켠 후, 네트워크 탭에서 온라인을 오프라인으로 바꿉니다.
2. Live2D-DCG 폴더 안의 viewerK.html 을 브라우저에 드래그 앤 드롭해서 뷰어를 엽니다.
3. 뷰어를 통해 원하는 차일드의 PNG 이미지 파일들을 얻습니다.
4. apngasm_gui 를 이용하여 animated PNG 파일을 만듭니다.
5. apng2gif_gui 를 이용하여 GIF 움짤 파일을 만듭니다.

각 항목에 대한 구체적인 설명은 Manual 폴더를 읽어보시기 바랍니다.


본 툴에는 용량의 문제로 차일드 언팩 파일의 대부분이 동봉되어 있지 않습니다. 
순정 차일드 언팩 파일은 https://github.com/Live2D-DCG/Live2D-DCG.github.io 를 다운받아 static/Korean 폴더에 있는 파일들을 그대로 쓰면 됩니다.


아래는 직접 차일드를 추가하는 방법입니다. 차일드를 언팩하는 방법은 생략하도록 하겠습니다.

1. unpack된 차일드 파일의 폴더를 Live2D-DCG/static/Korean 안에 복사합니다.
2. 조건에 맞게 아래의 설명대로 파일 이름을 변경하면 됩니다. (참고: https://github.com/Live2D-DCG/DCG/blob/master/Live2D%20Scripts)

txt 파일이 총 3개인 경우
00000000.txt -> [폴더_이름]_attack.mtn
00000001.txt -> [폴더_이름]_hit.mtn
00000002.txt -> [폴더_이름]_idle.mtn
00000003.moc -> character.dat
00000004.dat -> MOC.[폴더_이름].json

txt 파일이 총 3개인 경우
00000000.txt -> [폴더_이름]_attack.mtn
00000001.txt -> [폴더_이름]_banner.mtn
00000002.txt -> [폴더_이름]_hit.mtn
00000003.txt -> [폴더_이름]_idle.mtn
00000004.moc -> character.dat
00000005.dat -> MOC.[폴더_이름].json

모든 png 파일은 순서대로 texture_00.png, texture_01.png, ... 로 바꿔줍니다.

온천 데이터인 경우

00000000.moc -> character.dat
00000001.dat -> MOC.[폴더_이름].json
00000002.physics -> physics.json
00000003.txt -> [폴더_이름]_idle.mtn
00000004.txt -> [폴더_이름]_max.mtn
00000005.txt -> [폴더_이름]_maxtouch.mtn
00000006.txt -> [폴더_이름]_touch.mtn

마찬가지로 모든 png 파일은 순서대로 texture_00.png, texture_01.png, ... 로 바꿔줍니다.
