## 속성(Properties)

- HTML 속성(Attributes)
- CSS 속성(Properties)
- JS 속성(Properties)

## width, height 요소의 가로/세로 너비

- 기본값(요소에 이미 들어 있는 속성의 값): auto(브라우저가 너비를 계산)
- 단위: px,em,vw 등 단위로 지정

```html
대표적인 인라인요소 본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정하는
용도.
<span>Hello</span>
<span>World</span>

span의 auto는 포함한 콘텐츠 크기만큼 자동으로 줄어듬!
```

## max-width, max-height

- max-width,height

  - 요소가 커질 수 있는 최대 가로/세로 너비
  - none: 최대 너비 제한 없음 / 기본값
  - auto: 브라우저가 너비를 계산
  - 단위: px, em, vw 등 단위를 지정

- min-width,height

  - 요소가 작아질 수 있는 최소 가로/세로 너비
  - 0: 최소 너비 제한 없음 /기본값 0이고 0은 단위를 기재하지 않는다.
  - auto: 브라우저가 너비를 계산
  - 단위: px, em, vw 등 단위를 지정

- width와 height
  - width는 가로너비
  - height는 세로너비
  - 둘의 기본 값은 auto

```html
<div class="parent">
  <div class="child"></div>
</div>
div는 블럭요소이기 때문에 width와 height의 기본값이 auto이다.
```

```css
.parant {
  height: 200px;
  background-color: red;
}
.child {
  max-width: 300px;
  /* 자식요소이기 때문에 부모요소의 값을 따라 가지만
  max-width를 사용해 제한을 걸면 그 이상 늘어나지 못한다. 반대로  min을 하면 줄어들수 있는 크기가 제한된다.
  */
  height: 100px;
  background-color: blue;
}
```

## 단위: 표현단위

- px: 픽셀
- %: 상대적 백분율
- em: 요소의 글꼴 크기 /1em은 10px
- rem: 루트 요소(html)의 글꼴 크기 /최상위
- vw: 뷰포트 가로 너비의 백분율 /뷰포트: 브라우저 내 출력되는 전체화면 /1rvw은 가로너비의 100/1
- vh: 뷰포트 세로 너비의 백분율 /1rvh은 세로너비의 100/1

- 만약 width에 20em을 한다면?

  - html의 기본 폰트 사이즈의 값은 16이다. em은 10px이기에 16X10=160의 값이 나온다.
  - 만약 폰트사이즈의 값이 지정된다면 그 값의 em의 값을 곱하면 된다.

- em과 다른 rem

  - em을 사용하면 각각의 폰트 사이즈가 달라 어느 곳에 em의 값과 계산 적용되었는지 복잡해질수 있다.
  - rem의 최상위 html의 값의 폰트사이즈에만 계산을 한다.
  - 그렇기에 html에 폰트사이즈를 적용해놓으면 그 고정값에 항상 rem의 값이 계산되어진다.

- vw와 vh
  - width: 50vW는? 화면의 가로의 절반
  - height: 50vh는? 화면의 세로의 절반 100vh는 전체화면 늘어나거나 줄어도 항상 그 비율을 유지한다.

### 문제!

- em 단위의 기준은?

  - 해당하는 요소의 글꼴 크기

- 0px와 0vw 중 더 큰 값은?
  - 0 자체는 단위를 가지지 않기 때문에 단위와 상관없이 값은 동일하다.

## margin: 요소의 외부 여백(공간)을 지정하는 단축속성, 밖의 공간/ 음수를 사용할 수 있다./방향을 추가해 지정할수도 있다.ex) margin-bottom 외부 밑 여백

- 0: 외부 여백없음
- auto: 브라우저가 여백을 계산/ 가로(세로) 너비가 있는 요소의 가운데 정렬에 활용
- 단위: px,em,vw 등 단위로 지정
- %: 부모 요소의 가로 너비에 대한 비율로 지정/ 사용은 극히 드문 경우

### 마진의 기본 적용? (중요)

- 기본은 모두 적용 순서는 상, 좌, 하, 우 시계방향구조
- marign: 10p, 20px; / 2개의 값일 경우 상하, 좌우
- marign: 10p, 20px, 30px; 3개의 값일 경우 상, 좌우, 하
  - marigin: 상, 우, 하, 좌 /기본
  - marigin: 상하, 좌우 /2개
  - marigin: 상, 좌우, 하 /3개
  - marigin: 상, 우, 하, 좌 /4개
- 마진에 음수 -의 값을 쓰게 되면 떨어지기 보다 오히려 붙는다.

### 마진의 방향 margin-방향: 요소의 외부여백(공간)을 지정하는 기타 개별 속성들

- marigin-top, marigin-bottom, marigin-left, marigin-right

### 문제!

- margin 속성의 역할은?
  - 요소의 외부 여백
- margin: 40px 30px 20px; 일때 30px의 방향은?
  - 좌우
- margin: 20px 10px; 일때 20px의 방향은?
  - 상하

## padding: 요소의 내부 여백(공간)을 지정하는 단축속성 / 요소의 크기가 커진다.

- 0: 내부 여백 없음
- 단위: px, em, vw 등 단위로 지정
- %: 부모 요소의 가로 너비에 대한 비율로 지정

### 마진과 동일한 방향

- padding: 상, 우, 하, 좌
- padding: 상하, 좌우
- padding: 상, 좌우, 하
- padding: 상, 우, 하, 좌
- padding-top, padding-bottom, padding-left, padding-right

## 문제!

- padding 속성의 역할은?

  - 요소의 내부여백

- padding: 20px 10px 40px 30px;에서 30px은 어느 방향인가?

  - 좌 왼쪽

- padding 속성의 특징은?
  - 요소의 크기가 늘어남

## border: 요소의 테두리 선을 지정하는 단축 속성 선-두께 선-종류 선-색상; border-width,style,color

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container .item {
  width: 100px;
  height: 100px;
  background-color: red;
}
.container .item:first-child {
  border: 10px solid orange;
}
```

### border-width: 요소 테두리 선의 두께

- medium: 중간두께
- thin: 얇은 두께
- thick: 두꺼운 두께
- 단위: px, em, % 등 단위로 지정
- border-width: 상, 우, 하, 좌
- border-width: 상하, 좌우
- border-width: 상, 좌우, 하
- border-width: 상, 우, 하, 좌

### border-style: 요소 테두리 선의 종류

- none: 선없음/기본 \*
- solid: 실선(일반 선) \*
- dotted: 점선
- dashed: 파선 \*
- doudle: 두줄 선
- groove: 홈이 파여있는 모양
- ridge: 솟은 모양(groove 반대)
- inset: 요소 전체가 들어간 모양
- outset: 요소 전체가 나온 모양

### border-color: 요소 테두리 선의 색상을 지정하는 단축 속성

- black: 검정색/기본
- 색상: 선의색상
- transparent: 투명
