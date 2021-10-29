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
