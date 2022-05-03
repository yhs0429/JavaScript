# JavaScript

- HTML과 Server Script 사이에서 접속자의 마우스 클릭,키보드 입력 등 이벤트 처리를 주로 담당
- HTML+CSS <--->javascript<---->백엔드

​ 출력 동작/이벤트 데이터베이스 접속 처리 (Oracle,MySQL..)

- Ajax통신을 이용하여 비동기 통신이 가능하며 , jQuery로 Framework화 되어 발전 , 요즘은 통신의 결과를 SPA(Single Page Application)로 구현하기 위해 React를 사용함
- 참조 사이트 : [https://developer.mozilla.org/en-US/docs/Web/JavaScript]

## JS실행,VScode 설정

- js는 브라우저에서 확인할 수 있음
- 비주얼 스튜디오를 사용하여 코딩할수있음

```
>>>효율적인 코딩을 위한 Extentions
- open in browser install : 브라우저에서 확인
- Material Theme install -> set color theme -> darker high contrast
- Material Icon Theme install
- Prettier - Code formatter install -> 아래 부분 Manage -> Settings 선택 ->
    save 검색 후
          Editor:Format On Save 아래 체크
    prettier 검색 후
          Prettier :Tab Width
          Number of spaces it should use per tab
          2 로 설정
    Quote 검색 후
          Javascript;Preferences: Quote Style
          .....
          auto -> single로 변경

    Typescript;Preferences: Quote Style
          .....
          auto -> single로 변경
- Bracket Pair Colorizer install : 괄호 색깔 다르게 지정됨
- Indent Rainbow install : 들여쓰기가 보기 좋게 표현된다.
- Auto Rename Tag install : html의 앞에 태그를 바꾸면 뒤에 닫는 태그도 바꾸어준다.
- CSS Peek install : css 찾기 쉽게 한다. class의 이름 위에서 Ctrl + 클릭하면 style로 이동.
- HTML CSS Support install : html에서 css의 자동완성 이용할 수 있다.
- Live Server install : 서버사용, html, css 변경사항을 저장후 바로 적용해준다.
        Manager -> Settings -> live server 검색 -> Use local ip 체크, Custom Browser : chrome선택

        html 파일의 Open with Live Server 선택 후 브라우저에서 확인할 수 있다.
```

## async 와 defer

- HTML 한줄 한줄 읽어가는것(이해,분석)을 parsing 이라고 함

```
<script src='main.js'></script>
html parsing > js다운 > js실행 > 다시 html parsing
페이지가 준비되기 전 js가 실행 될 수 있음, js 파일이 크면 페이지 준비까지 오래걸릴수있음


<script async src='main.js'></script>
html parsing > blocked > html parsing > js다운 > js실행
병렬로 html parsing과 js다운로드 가 된다 그러나 페이지가 준비되지 않은 상태에서 js가 다운로드되어 실행될 수 있음


<script defer src='main.js'></script>
html parsing    ┐
                   >  페이지 보여줌 > js실행
js다운로드        ┘
병렬로 html parsing과 js가 다운로드 되고 js가 실행된다 가장 안정적인 방법!!!!
여러개의 js는 다운로드 시간과 상관없이 선언된 순서대로 실행됨
```
