
---
- `position: absolute;`가 사용된 요소는 디스플레이 값이 자동으로 변한다.
- `display : block`
- `position: fixed`도 동일하게 `block`으로 변경된다.
```css  
header .sub-menu ul.menu li {
  position: relative;
}  

header .sub-menu ul.menu li::before {
  content: "";
  display: block;
  width: 1px;
  height: 12px;
  background-color: black;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto 0;
}
```