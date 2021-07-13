# 프론트 엔드 개발
## 클라이언트-서버 시스템(모델)

> 클라이언트 - 서버 시스템은 복잡한 네트워크 연결중 양 끝단에 연결된 사용자와 공급자의 관계를 의미함
> 
> 클라이언트 : 사용자가 사용하는 디바이스 또는 디바이스에서 실행되는 어플리케이션
> 
> Ex) 웹 브라우저
> 
> 서버 : 데이터, 네트워크 서비스가 공급되는 디바이스 또는 디바이스에서 실행되는 서버소프트웨어
> 
> Ex) 아파치 서버

## HTML
> HTML - Hyper Text Markup Language
> 
> 웹페이지에 구성 요소를 표시하는 언어
> 
> 구성 요소 : 콘텐츠, 구조

## HTML 기본구조

`(backtick)

```
<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>
```

- DOCTYPE : html문서 타입
- html : html 영역표시
- head : 해당 웹페이지의 부연설명, 부가정보가 포함
- body : 웹페이지의 콘텐츠를 표시하는 영역

## HTML 요소 기본 개념

### HTML 요소 문법
 
 ```
   <starttag>contents</endtag>
 ```
 
 ### 포함관계
 
 > 요소의 영역안에 다른 요소를 포함하는 관계
 > 
 > 포함하는 요소 : 부모(parent)요소
 > 
 > 포함되는 요소 : 자식(child)요소
 > 
 > 직계가 아닌 포함하는 요소 : 조상(ancestor)요소
 > 
 > 직계가 아닌 포함되는 요소 : 자손(descendant)요소 

### Empty element (빈 요소)
> 시작태그만 있고 종료 태그가 없는 요소

### HTML 속성 (Attributes)
> html element 에 대해 추가정보(이동경로, 파일명...)를 제공
> 
> 시작태그에 입력
> 
> 형식 : 속성이름 = "속성값"

### HTML로 표현할 수 있는 컨텐츠 (웹페이지에서 표현할 수 있는 컨텐츠)
> 텍스트
> 
> 멀티미디어 컨텐츠 (이미지, 비디오, 오디오)

### 제목 요소 (Heading Element)
> h1 ~ h6 (h : heading)

### 단락 요소 (Paragraph Element)
> p : Paragraph

> hr : horizontal rules
> 
> - 단락을 구분하는 수평선을 표시
> 
> 빈요소

> br : Line Break
> 
> - 같은 단락안에서 강제 줄바꿈을 할 때
> 
> 빈요소

### 하이퍼링크 요소 (Hyper Link Element)
> a : anchor

```
<a href="http://www.naver.com">링크텍스트(본인이 원하는 명명법으로 작성)</a>
```

> href : hyper text reference - 이동하고자 하는 목족이 위치/경로를 표시하는 속성
> 
> - URL(Uniform Resource Locator) : 이동하고자 하는 목적지(웹페이지)의 위치/경로 값

###목록 요소(List Element)
> 순서있는/ 순서없는 목록
> - ol(순서 있는), ul(순서없는), li(각각 리스트)

> 설명 목록
> - 주제와 설명이 한 세트로 구성되는 목록
> - dl(설명 목록 열기&닫기), dt(설명할 단어), dd(설명문)

### 북마크
> 북마킹 하고 싶은 곳에(보여주고 싶은 장면) <a href="#적당한 이름"> </a> 을 적는다
> 북마크 클릭하고 싶은 곳에 <id="이미 설정된 이름"> 을 적는다. ex) <h2 id="적당한 이름">

### Table Element (https://www.tablesgenerator.com/html_tables)
> table, thead, tbody, tfoot, tr, th, td, caption

  
```  
 <table>
   <caption></caption>
   <thead>
     <tr>
       <th></th>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td></td>
     </tr>
   </tbody>
   <tfoot>
     <tr>
       <td></td>
     </tr>
   </tfoot>
  </table>
```

> table : table 의 영역을 설정
  >
> theadm tbody, tfoot : table 데이터 그룹을 표시
  >
> tr(table row) : 표의 가로줄
  >
  > th(table head) : 제목 칸(셀)
  >
  > td(table data) : 데이터 칸(셀)
 
### Image element
  > img (image)
  > attribute : src (source), alt (alternative)
  
  ```
  <img src="파일명.jpg" alt="설정하고 싶은 이름(보통 사진{이미지}의 특성으로 지음)">
  ```
  
  > img 태그를 사용할 때 src, alt 속성은 반드시 사용해야 함
  
  ### Video Element
  > attribute
  > - controls : 비디오 컨트롤 버튼 표시
  > - loop : 비디오 반복 재생
  > - muted : 음소거
  > - autoplay : 자동재생 (항상 muted 와 같이 사용해야만 함)

### 절대 경로/상대경로

  > 절대경로 : 컨텐츠 파일을 불러오고자 하는 HTML 페이지가 어던 위치에 있던간에 동일하게 찾아올 수 있도록 자세하게 표시하는 경로
  > 상대경로 : 컨텐츠 파일을 불러오고자 하는 HTML 페이지의 위치를 기준으로 컨턴츠 파일의 위치를 표시하는 경로
  
  ```
  >절대경로 : <img src="https://w3schools.com/images/picture.jpg">
  >상대경로 : <img src="images/picture.jpg">
  ```
  
### Block/Inline Element
  > 화면에 표시되는 형태를 기준으로 구분하는 방식
  
  > Block Element
  > - 화면에 줄바꿈되어 표시되는 요소
  > - 항상 사용가능한 전체 너비를 차지함
  > 
  > Inline Element
  > - 화면에 줄바꿈되지 않고 나란히 표시되는 요소
  > - 인라인 요소에 포함된 콘텐츠의 너비만큼만 차지함
  
 ### 폼 요소
  > input, button
  
  ```
  <input type="text">

<input type="password">

<input type="button" value="이름">
<input type="submit" value="이름">
<input type="reset" value="이름">

<button type="button">이름</button>
<button type="submit">이름</button>
<button type="reset">이름</button>
  ```

### 인터넷 주소 체계
  > IP address : 192.168.0.1
>
> Domain address : https://www.naver.com
>
> 기본주소(IP) => 의미있는 영어단어로 변환 : 도메인 주소
> www.naver.com/images/picture.jpg => URL
  
  
  ###CSS
  > CSS(Cascading Style Sheet)
>
> cascading : 나중에 선언한것이 최종 반영되는 CSS 특징
>
> CSS는 여러 대상에 대해서 공통으로 스타일을 적용시킬수 있음
  
 > CSS syntax
>
> selector(선택자)와 declaration block(선언블록)으로 구성됨
>
> 선언블록은 중괄호 안에 여러 선언을 포함
>
> 각 선언에는 property와 value로 구성됨
  
  ```
  h1 {color:red;font-size:10px;}
  ```
  
  ### Class, id
  > HTML element에 대해서 이름을 지정해줄 때 사용하는 attibute

> class
>
> - 여러개의 HTML element에 같은 클래스 이름을 사용할 수 있음

> - 한 개의 HTML element에 여러개의 클래스 이름을 사용할 수 있음

> id

> - id 이름은 HTML 문서내에서 고유해야함(한 개만 존재)

> - 한 개의 HTML element에 한 개의 id 이름만 사용할 수 있음

  ```
  <div class="box box1 box2"></div>
<div class="box box1 box2"></div>
<div class="box box1 box2"></div>

<div id="title1"></div>
<div id="title2"></div>
<div id="title3"></div>
  ```
  
  ### Naming 표시 방식
  > - naming을 할 때 한 단어로 naming을 하기에는 한계가 있기 때문에 여러 단어로 naming을 하게될 때, 단어와 단어 사이를 구분해야 하는데 일반 문서 작성처럼 띄어쓰기로 구분할 수 없기때문에 단어와 단어 사이를 기호나 규칙에 의해서 띄어쓰지 않고 구분할 수 있도혹 함 => 표기방식
  
  > 표기방식 종류

> - snake case : gnb_list_item (underbar/underscore) => file/folder
> - kebab case : gnb-list-item (hyphen/dash) => id/class
> - camel case : gnbListItem => javascript 변수/함수 이름
> - Pascal case : GnbListItem => javascript에서의 class 이름 지정
  
  ```
  코딩은 왼쪽에서 오른쪽, 위에서 아래로 순서로 한다.
  ```
  
  
  
