# JavaScript

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

* document.getElementById() 예시

```javascript
<script>
window.onload = function(){
	var header = document.getElementById('header')
    header.style.color = 'orange';
    header.style.background = 'red';
    header.innerHTML = 'From JavaScript';
}
</script>
</head>
<body>
    <h1 id="header">Header</h1>
<body>
```

### 글자 속성

| 속성        | 설명                                                     |
| ----------- | -------------------------------------------------------- |
| textContent | 문서 객체 내부 글자를 순수 텍스트 형식으로 가져오도록 함 |
| innerHTML   | 문서 객체 내부 글자의 HTML태그를 반영해 가져오도록 변경  |

```javascript
<script>
	window.online = function(){
		var output = '';
		for (var i=0; i<10; i++){
			output +='<h1>Header - '+i+'</h1>';
		}
		document.body.textContent = output; // 1번
		//document.body.innerHTML = output; // 2번
	};
</script>
```

* 1번과 같이 적용한 경우 \<h1>태그가 텍스트로 직접 나오게 된다.
* 2번과 같이 적용할 경우 \<h1>태그가 적용되어 나오게 된다. 

### 속성 조작

| 메소드                           | 설명      |
| -------------------------------- | --------- |
| setAttribute(속성 이름, 속성 값) | 속성 지정 |
| getAttribute(속성이름)           | 속성 추출 |



### 이벤트 모델

| window-브라우저창               | onload                                                  | html문서 로딩 완료 이벤트                                    |
| ------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------ |
| 모든 태그                       | onclick<br />ondbclick<br />onmouseover<br />onmouseout | 태그 클릭<br />더블클릭<br />마우스가 올려진 상태<br />마우스가 올려졌다 이동된 상태 |
| input<br />type=text/password   | onkeydown<br />onkeypress<br />onkeyup                  | 키보드 입력                                                  |
| input<br />tyope=radio/checkbox | onchange                                                | 상태변화 이벤트                                              |
| input type=submit               | onsubmit                                                | 폼 양식 입력                                                 |

<a href=""

클릭하면 href 지정 url로 이동 기능 내장 태그

클릭이벤트 = function(){href지정 url로 이동}

* 기본적으로 이동하는 기능을 없앨 수도 있다. 

```html
button.onclick=function(){
	return false;
} // 또는

button.onclick=function(e){
	e.preventDefault();
}
```

### var, let, const

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