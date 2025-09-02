- 자바스크립트는 웹 문서를 제어하기 위해 개발된 언어
- 브라우저는 웹 문서를 해석할 수 있는 렌더링 엔진이 있다.
- 렌더링엔진이 html로 작성된 문서를 한줄한줄 해석
- 객체화 하여 자바스크립트로 접근 가능하게 만든다.

이를 **DOM(Document Object Model) 문서 객체 모델**이라고 한다. 
이를 통해 스크립트 언어로 HTML 요소를 제어할 수 있다.

### 1. DOM의 구조적 특징

- DOM은 **트리(Tree) 구조**로 표현된다.  
    → HTML 문서 전체가 루트 노드(`document`)로 시작하고, 태그들은 부모-자식 관계로 연결됨.
    
- 각 HTML 태그는 **노드(Node)**로 취급되며, 종류가 있음:
    - **Element Node**: `<div>`, `<p>` 같은 태그 요소
    - **Text Node**: 태그 안의 텍스트 내용
    - **Attribute Node**: 태그의 속성(`id`, `class`, `src` 등)
## TREE 구조
---
- 웹 브라우저는 HTML 문서를 해석할 때 **트리 구조**로 변환
- 이 트리는 **문서 객체 모델(DOM)**로 불리며, 각 요소에 자바스크립트로 접근·제어할 수 있게 만든다.
```html
<html>
  <body>
    <h1>Hello</h1>
    <p>World</p>
  </body>
</html>
```
위 문서는 아래처럼 트리 구조로 표현된다:

- **Root:** `document`    
    - **Child:** `<html>`        
        - `<body>`            
            - `<h1>` → `Hello` (텍스트 노드)                
            - `<p>` → `World` (텍스트 노드)


> **Tree(트리)** 는 **계층적(hierarchical) 자료구조**. 
> **루트(root)** 에서 시작해 **노드(node)** 들이 연결
> 각 노드는 **부모(parent)** 와 **자식(children)** 관계를 가짐.


## BOM(Brower Object Model)
---
브라우저를 제어할 수있도록 모델링한것  
> css를 자바스크립트로 조작 할수 있는 것을 **CSSOM**이라고 한다.

- **DOM**: HTML 문서 구조를 객체로 표현한 모델    
- **BOM (Browser Object Model)**: `window`, `navigator`, `location` 같은 **브라우저 자체**를 제어하는 모델  
    → DOM과 BOM을 함께 사용해 웹페이지 전체를 제어 가능.