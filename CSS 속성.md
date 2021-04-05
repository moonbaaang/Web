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
