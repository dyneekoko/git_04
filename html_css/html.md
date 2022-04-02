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
