
- `document.getElementById` : HTML 문서에서 고유한 ID를 할당
- `document.getElementsByClassName`
- `document.getElementsByTagName`

```html
<body>
    <section>
      <h2 id="title">운동</h2>
      <form action="" name="myForm">
        <input type="text" name="myText" id="" />
        <button>추가</button>
      </form>
      <ul class="list">
        <li class="item">스쿼트</li>
        <li class="item">벤치프래스</li>
        <li class="item">데드리프트</li>
      </ul>
      <p class="hello">안녕하세요</p>
    </section>
  </body>
```

```js
const title = document.getElementById("title");
console.log(title);
title.textContent = "헬스 3대 운동";
```

![[Pasted image 20250902223029.png]]
## DOM 요소 쿼리

`querySelector`, `querySelectorAll`은 CSS 요소 선택자를 사용해 요소를찾는다.

