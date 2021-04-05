# CSS 속성

### 박스속성

* margin / border / padding / width / height 을 모두 합쳐 박스 속성이라고 한다.
* left, right, top, bottom 으로 구분하여 설정 가능하다. (margin, border, pedding)
  * 테두리를 넣을 때는 두께, 형태, 색상에 맞는 속성을 사용한다.
    * ex) border-width, border-style, border-color 
    * 이러한 형태로도 가능하다.
      * border: \<width> \<style> \<color>
    * radius - 테두리에 둥글기를 적용시킨다.

### 가시속성

* none / block / inline / inline-block
  * inline형식은 margin과  padding속성을 좌우로만 설정할 수 있다.

### 배경속성

| 속성                  | 설명                | 비고          |
| --------------------- | ------------------- | ------------- |
| background-image      | 배경이미지 삽입     |               |
| background-size       | 크기 지정           |               |
| background-repeat     | 반복 형태 지정      | no-repeat     |
| background-attachment | 부착 형태 지정      | scroll, fixed |
| background-position   | 위치 설정           | 키워드 or x y |
| background            | 모든 배경 속성 입력 |               |

### 글자 속성

| 속성            | 설명        | 비고                    |
| --------------- | ----------- | ----------------------- |
| font-size       | 글자 크기   | px, em, large, small 등 |
| font-family     | 글꼴 지정   | 글꼴 여러개 지정 가능   |
| font-style      | 글꼴 스타일 | 기울기 등               |
| font-weight     | 글꼴 두께   |                         |
| text-align      | 글자 정렬   | center, left, right     |
| text-decoration | 글자 꾸미기 | none: 밑줄만 제거       |

### 위치속성

* ex) position : absolute

| 키워드   | 설명                                |
| -------- | ----------------------------------- |
| absolute | 절대위치 좌표 설정                  |
| fixed    | 화면을 기준으로 절대 위치 좌표 설정 |
| relative | 초기 위치에서 상하좌우 위치 이동    |
| static   | 위쪽에서 아래쪽으로 순서대로 배치   |

* z-index : 물체를 겹쳐서 놔둘 시 앞에 오는 물체를 결정할 수 있다.

* 자손의 position속성에 absolute 키워드를 적용하려면 부모의 position 속성에 relative 키워드를 적용하거나 height속성을 입력한다.

* 내용이 요소 크기를 벗어날 때
  * overflow : hidden, scroll;
  * overflow-x, overflow-y 적용 가능

### 유동 속성

* float속성 - 태그를 수평정렬합니다.

```css
<style>
	img { float:left; }
</style>
```

### 그림자와 그레디언트 속성

* 글자에 그림자 부여
  * ex) text-shadow : 5px 5px 3px black
* 박스에 그림자 부여
  * ex) box-shadow : 5px 5px 3px black
* 쉼표를 사용하면 그림자 속성을 여러 개 적용할 수 있다.

### html5

| html태그            | css                   | javascript                                                   |
| ------------------- | --------------------- | ------------------------------------------------------------ |
| 화면 구성 요소 나열 | 크기, 색상, 위치 결정 | 기능 추가                                                    |
| 정적 페이지 구성    |                       | 동적 페이지 구성<br />= html 태그 변경                       |
|                     |                       | html태그를 읽어 기능을 추가하면<br />화면이 동적으로 변경<br />document object model (dom 객체)<br />(문서 객체 모델) |

* DOM의 형태
  * html 태그는 계층 구조

```html
<script> 자동생성 </script>
var body = {innerHTML : a, , }
var a = {
    href : "www.naver.com",
    innerHTML:"링크",
    ...
}
<body>
    <a href="naver.com"> 링크 </a>
</body>
```

* <태그명 속성명1 = 값1 ..>
* <태그명 속성명1 = 값1 ..> 내용(=바디)-innerHTML </태그명>

* var 태그명 = {속성명1=값1, ...}
* DOM레벨 1
  * 고전 이벤트 모델 : 자바스크립트 내부에 작성
  * 인라인 이벤트 모델 : 태그 내부에 작성

## 문서 객체 모델

> 태그를 자바스크립트에서 사용할 수 있는 객체로 만든 것

문서 객체를 조작한다는 것은 결국 태그를 조작한다는 것이다.

* 트리의 각 요소를 노드 라고 한다.

### 문서 객체 선택

| 구분     | 메서드                                | 설명                       |
| -------- | ------------------------------------- | -------------------------- |
| 1개 선택 | document.getElementById(아이디)       | 아이디로 1개 선택          |
|          | document.querySelector(선택자)        | 선택자로 1개 선택          |
| 2개 선택 | document.getElementsByName(이름)      | name 속성으로 여러개 선택  |
|          | document.getElementsByClassName(이름) | class 속성으로 여러개 선택 |
|          | document.querySelectorAll(선택자)     | 선택자로 여러 개 선택      |



### 이벤트 모델

| window-브라우저창               | onload                                                  | html문서 로딩 완료 이벤트                                    |
| ------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------ |
| 모든 태그                       | onclick<br />ondbclick<br />onmouseover<br />onmouseout | 태그 클릭<br />더블클릭<br />마우스가 올려진 상태<br />마우스가 올려졌다 이동된 상태 |
| input<br />type=text/password   | onkeydown<br />onkeypress<br />onkeyup                  | 키보드 입력                                                  |
| input<br />tyope=radio/checkbox | onchange                                                | 상태변화 이벤트                                              |
| input type=submit               | onsubmit                                                | 폼 양식 입력                                                 |
|                                 |                                                         |                                                              |

<a href=""

클릭하면 href 지정 url로 이동 기능 내장 태그

클릭이벤트 = function(){href지정 url로 이동}

* 기본적으로 이동하는 기능을 없앨 수도 있다.

let, const

| var =10;<br />var a="a" | let a= 10;<br />let a= "a" >> error<br />let b = 10;<br />b = "a" 이는 가능 | const a = 10<br />a = "a" >> error |
| ----------------------- | ------------------------------------------------------------ | ---------------------------------- |
|                         | ECMASCRIPT6 에서 추가                                        | ECMASCRIPT6 에서 추가              |

* ECMASCRIPT6 함수
  * 화살표 함수 (java lambda식)
    * 매개변수 -> {문장} > 메서드 이름이 없어도 실행 가능
    * 이를 자바스크립트에서 화살표 함수 라고 부른다.
      * 간단한 문장으로 구성된 메소드를 정의/호출
    * (매개변수) => {문장} (화살표 모양 주의)ㄴ

* ECMASCRIPT5 에서 추가된 함수
  * Array.forEach(function(one){ ... }); >> 반복문 구현하지 않아도 내부적으로 반복