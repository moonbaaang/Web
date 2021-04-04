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

| 속성        | 설명        | 비고                    |
| ----------- | ----------- | ----------------------- |
| font-size   | 글자 크기   | px, em, large, small 등 |
| font-family | 글꼴 지정   | 글꼴 여러개 지정 가능   |
| font-style  | 글꼴 스타일 | 기울기 등               |
| font-weight | 글자 두께   |                         |
| text-align  | 글자 정렬   | center, left, right     |

