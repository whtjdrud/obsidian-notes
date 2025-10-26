
## 💻 전체 코드

### HTML
```html
<div class="container">
  <div class="item"></div>
</div>
``` 
### CSS
```css
.container {
  width: 600px;
  height: 300px;
  background-color: royalblue;
  position: relative; /* 중요! */
}

.item {
  width: 100px;
  height: 100px;
  background-color: orange;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
}
```

  
## 🧩 동작 원리
### 1️⃣ position: absolute
---
- 부모(.container) 기준으로 위치를 제어할 수 있게 함.  
- 부모 요소에는 반드시 `position: relative`가 필요.

### 2️⃣ top, bottom, left, right = 0
---
- **요소를 부모의 네 방향 끝까지 늘릴 수 있는 상태**로 만듦.  
- 즉, 상하좌우 **여백을 모두 0으로 설정**.
  

### 3️⃣ margin: auto
---
- `margin: auto`는 **남는 여백을 자동으로 균등 분배**함.  
- 단, height와 width가 명확히 정의되어 있어야 함.  
  → 그렇지 않으면 여백 계산이 불가능함.

## 🧠 추가로 알아두면 좋은 내용

### 1️⃣ 부모의 position
---
- 부모가 `static`이면 자식의 `absolute` 기준이 **body로 이동**함.  
  → 중앙정렬이 깨짐.  
  → 반드시 부모에 `position: relative;` 설정.

### 2️⃣ width / height가 없는 경우
---
- 자동 중앙정렬 불가능.  
- 브라우저가 `margin: auto` 계산 시 **요소의 고정 크기**가 필요하기 때문.
