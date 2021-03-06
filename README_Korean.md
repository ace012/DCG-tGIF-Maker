# DCG tGIF Maker


## 설명

본 툴은 약간 수정된 뷰어 사이트 (https://DCG-tGIF.github.io/) 를 통해 데스티니 차일드 캐릭터의 투명 배경 이미지 파일을 프레임 단위의 PNG 파일로 추출할 수 있습니다. 이를 통해 원하는 차일드의 투명 배경 움짤을 만들 수 있습니다.

이 툴은 데스티니 차일드 캐릭터 Live2D 뷰어 사이트인 Live2D-DCG.github.io (https://github.com/Live2D-DCG/Live2D-DCG.github.io) 사이트를 수정하여 만들어졌습니다.

또한, 브라우저에서 이미지들을 압축하여 한번에 다운로드받을 수 있도록 하기 위해 JSZip (https://stuk.github.io/jszip/) 를 차용하였습니다.


## 사용법

아래는 움짤을 만드는 순서입니다.

    1. 뷰어를 통해 원하는 차일드의 PNG 이미지 파일들을 얻습니다.
    2. apngasm_gui 를 이용하여 animated PNG 파일을 만듭니다.
    3. apng2gif_gui 를 이용하여 GIF 움짤 파일을 만듭니다.

각 항목에 대한 구체적인 설명은 Manual 폴더를 읽어보시기 바랍니다.


## 커스텀 텍스처 적용시키기

아래는 커스텀 텍스처 이미지를 적용시키는 방법입니다.

    1. 텍스처 이미지 파일의 이름을 texture_00.png 로 바꿔줍니다.
      1-1. 만약 텍스처 이미지가 2개 존재한다면,  파일 이름 순서대로 texture_00.png, texture_01.png 로 바꿔줍니다.
    2. 뷰어 최하단의 파일 선택 버튼을 누른 후, 텍스처 이미지 파일을 불러옵니다.
