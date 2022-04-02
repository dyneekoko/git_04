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

```
<a href="url" target="_blank">텍스트</a>
  url = 인터넷 주소
```
  -target attribute는 blank만 사용 : 새탭열기
  -URL이란? : Uniform-한결같은 Resource-자원 Locator-위치
    -파일 위치 식별자
    - 웹페이지는 파일로 만드니 - 파일위치를 찾아가는 것