#html

- hyper text markup language
- HTML을 사용해서 웹페이지에 컨텐츠와 구조를 표시

## HTML basic

```
  <!DOCTYPE html> : 문서(웹페이지 문서들) 타입(종류) - 버전(HTML5 - W3C에서 확인)
  <html> : 웹 페이지 전체 영역
    <head> : 웹 페이지의 추가 정보(meta), 파일 임포트
      <title></title> : 꼭 넣어야함
    </head>

    <body> : 웹 페이지의 본문 영역 - 웹 페이지의 모든 콘텐츠를 표시하는 영역
    </body>
  </html>
```

## HTML syntax : 문법

- Tag를 사용해서 element를 표시/표현

```
  <tag> content </tag> : tag는 모두 소문자로 입력, 시작태그와 종료태그로 구성
  <tag> : 시작 태그만 존재하는 경우를 빈요소라고 함(Empty Element)
```

- 포함관계(Nesting, Nested Element)
  - Tag 영역안에 다른 Tag가 포함되는 것
  - 들여쓰기로 시작과 끝의 구분을 해줄 것(안해도 되지만 사람간의 확인차)
  - 포함하는 요소 : 조상요소(ancestor), 부모요소(parent)
  - 포함되는 요소 : 자손요소(descendant), 자식요소(child)

```
<html>
  <head></head>
  <body>
    <h1>큰제목</h1>
    <p>본문 내용</p>
  </body>
</html>

html 기준
  - 자식요소 : body
  - 자손요소 : h1, p
body 기준
  - 조상요소 : 없음
  - 부모요소 : html
  - 자식요소 : h1, p
  - 자손요소 : 없음
```

-Attribute(속성)
- tag에 필요한 추가정보를 알려주는 것
- attr 이름 = "필요한 값" (아닌경우도 있음)
- 

```
<tag attr="value"></tag>
```

## Text contents Markup

### heading(제목)
  - h : 태그 'h'eading 
  - h1 ~ h6

### Paragraph(단락)
  - P : 태그 'p'aragraph
```
WYSIWYG(What You See Is What You Get) : 보는 화면과 작업 화면이 같은 것
  -하지만 html은 태그로 표현하기에 wyw가 지원 안됨
  -요즘은 이 표현을 안씀 (파워포인트)
```
  - 강제 줄바꿈 : 'br'eak 태그
    - 시작태그만 존재하는 빈요소(Empty Element)
    - 강제 공백 : &nbsp; nonbrakespace; (엔터티 코드)

     -  < =	less than	&lt; &#60;	
     -  > = greater than	&gt; &#62;	
     -  &	= ampersand	&amp;	&#38;	
     -  "	= double quotation mark	&quot; &#34;	
     -  '	= single quotation mark (apostrophe)	&apos; &#39;

```
& : ampersand
앤터티코드 : 대체코드
  -특수문자를 직접 사용하지 못할 경우, 대체해서 사용하는 코드
```

-수평선 (horizontal Rule) : hr
  -단순하게 줄을 긋는것이 아니라, 단락을 구분하는 구분선

### HTML Link
- a : 'a'nchor 닻_바다용어 하이퍼링크 연결하는 태그
- href(hyper text reference) : 목적지 정보 속성(attribute)
  -reference : 참조
- bookmark : 연결된 페이지로 이동하지 않고, 같은 페이지 내에서 이동


```
- Page Link
<a href="url" target="_blank">텍스트</a>
  url = 인터넷 주소, 상세주소

- bookmark Link
  -Link : <a href="#target">목적지</a>
  -Target : <h2 id="target">단락의 제목</h2>


```
  -target attribute는 blank만 사용 : 새탭열기
  -URL이란? : Uniform-한결같은 Resource-자원 Locator-위치, 구분자
    -파일 위치 식별자
    - 웹페이지는 파일로 만드니 - 파일위치를 찾아가는 것
  
```

  - url 인터넷 주소체계 _ 기본
    - IP (internet protocol) address 
      : 인터넷 통신 주소 약속
        - 단점: 숫자라서 기억하기가 어렵다. (이름이 없기 때문)
    - Domain name : IP 주소를 영어 단어로 표현한 것
      - 서버종류 : www
      - 회사이름 : naver, kakao, daum
      - 기관성격 : com, net (3자리) / co, go, ac (4자리)
      - 국가(4자리) : kr, uk, ca, fr ..
      
    참조: 인터넷 역사

```




- 0~255까지 숫자 4개로 구성
  ex) 192.222.0.1

- 인터넷 접속 프로세스 
  주소표시줄에 -  Domain Name > IP주소로 변환 > 접속 

-URL 체계
  IP또는Domain / 상세경로 / 파일 정보
  ex) https://www.w3schools.com/html/default.asp
  도메인만 있어도 URL.
  
  W3C - HTML_Link
  More on Absolute URLs and Relative URLs
  ```

- HTML Links - Create Bookmarks
  ex) One Page Website
  : 스크립트와 연동하여 사용 - 한페이지에서 



### HTML Tables(요즘 많이 안씀): 모바일에서 대응이 안 됨
    html table generator > https://www.tablesgenerator.com/html_tables
    사이트 사용법 : WZW 마우스로 보는대로 만들어서 가져옴, 소스를 복사
    웹접근성 표현 어려움 , 모바일 대응이 안 됨
    
```
<table>
  <tr> : table row ~ 행
    <th></th> : table header - 열제몽
  </tr>
  <tr>
    <td></td> table data - 데이터
  </tr>
<table>




```
emmet wrap with


### HTML Lists
  - unordered list -> ul, li (order = 순사 : un = 순서 없는 목록)
    - 기호로 표시 된다. (중간점)
  - ordered list -> ol, li (순서 있는 목록)
    - 한글, 알파벳, 숫자로 표시 된다. (1.~,  2.~,  3.~)
  - li(List Item) : 목록 아이템
  - 중첩목록 (Nested List)
    - 목록 안에 작은 목록이 포함 되는 경우
    - 

  ```
  <ul> 
    <li>Html</li>
    <li>CSS</li>
    <li>JS</li>
  </ul>

  <ol>
    <li>Html</li>
    <li>CSS</li>
    <li>JS</li>
  </ol>

  ```

- Description List : 설명 목록 (세트로 사용해야 하는 목록들이 있음)
  - dl(Description List)
  - dt(Description Title)
  - dd(description date)

```
<dl>
  <dt></dt> : 목록의 주제
  <dd></dd> : 목록의 설명
</dl>

세트로 구성해야하는 설명 목록, 포함되지 않음, 부제목 같은 느낌
```


# HTML Multimedia
  -mp4(video), mp3(audio) : 모바일에서 사용할 수 있는 포멧들
  -image, video, audio content : embed content

### HTML Image
```
  - img attribute = src(source)
  - ex: <img src="www.naver.com/html/photo.jpg" alt="대체문구">
  - alt(alternative) : 대체 텍스트, 이미지를 볼 수 없기 때문에 
     스크린 리더에서 읽을 때에 더 중요
  
  - 이미지 형식
    - 비트맵 (포토샵), 벡터(일러스트레이터) 이미지 , 
      점(색상표현우수)과 좌표(사이즈에 우수)
        - jpg : 원본색상을 압축하는 표현에 우수
        - png : 투명배경 적용
        - gif : 용량이 작음, 색조합이 작음, 에니메이션을 만들 수 있음
        - svg : 벡터 형식 - 텍스트형식 -> 브라우저가 이미지로


```

### HTML Video : 스트리밍 사이트에 있는 것, HTML Audio는 활용빈도 떨어짐
  - video 사용하는 attribute
    autoplay, muted, poster, loop, controls
```
<video>
  <source src="파일경로/video.mp4" type="video/mp4">
</video>
```

시멘틱요소
```
<article> : 독립적으로 사용이 가능해야함
<aside>
<figure> : 그림형태의 컨텐츠를 그룹핑하는 요소
<footer>
<header>
<nav>
<section>
```

div, span : container 단순 그룹해주는 요소

```
https://www.w3schools.com/html/html_blocks.asp
```

### Container Element
  - 단순 구역을 나누는 그룹핑해주는 요소
  - div(division) : 구분하다 나누다
  - span : 범위(폭)의 의미
  
