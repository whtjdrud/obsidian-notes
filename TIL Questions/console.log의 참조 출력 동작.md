
관련내용 : [[HTML 요소 선택]]

## 질문 내용
---
```js
const title = document.getElementById("title");
console.log(title);
title.textContent = "헬스 3대 운동";
```
- 원래 title은 **운동**
- console.log에 title 이 2번재 줄인데??
- 실제 콘솔 창에는  헬스 3대 운동이 출력되었다.

## 코드 실행 순서
---
```js
const title = document.getElementById("title");
console.log(title);
title.textContent = "헬스 3대 운동";
```

- **`getElementById` 실행**    
    - DOM에서 `<h2 id="title">운동</h2>` 요소를 찾아 `title` 변수에 **그 요소 객체(참조)**를 담음.        
    - 즉, `title`은 문자열이 아니라 실제 `<h2>` 노드 객체를 가리킴.        
- **`console.log(title)` 실행**    
    - 브라우저 콘솔에 `title` 객체(노드)를 출력함.        
    - 여기서 중요한 건 `console.log`가 값을 "복사"해서 출력하는 게 아니라 **참조(Reference)**를 출력한다.        
- **`title.textContent = "헬스 3대 운동";` 실행**    
    - 이제 DOM의 내용이 `"운동"`에서 `"헬스 3대 운동"`으로 바뀜.

## 왜 "헬스 3대 운동"이 보이는가?
---
브라우저 콘솔은 단순히 "그 시점의 값"을 찍어두는 게 아니라,  
**참조된 객체의 현재 상태를 반영해서 보여주기 때문**

- `console.log(title)` 찍을 때는 `<h2>` 요소 참조가 출력됨.

- 이후 `textContent`가 바뀌면, 콘솔에서 그 참조된 요소를 열어봤을 때 최신 값 `"헬스 3대 운동"`이 보이는 거야.

👉 즉, **console.log가 늦게 실행된 게 아니라 콘솔이 참조 객체의 최신 상태를 보여주는 것**.


```js
console.log(title.textContent); // "운동"

title.textContent = "헬스 3대 운동";
```
로그에 **값 자체**를 출력하면 운동이라는 값이 출력된다.

## 다시 한번 정리
---
- `console.log`가 값을 "복사"해서 출력하는 게 아니라 **참조(Reference)**를 출력한다.  