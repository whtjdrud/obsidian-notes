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
![[Pasted image 20250902220618.png]]

이 DOM 요소를 통해 각각 접근하고 제어할 수 있다.

- **Tree(트리)**는 **계층적(hierarchical) 자료구조**.    
- **루트(root)**에서 시작해 **노드(node)**들이 연결되고, 각 노드는 **부모(parent)**와 **자식(children)** 관계를 가짐.

##### 용어
- **Root (루트):** 트리의 최상위 노드 (부모가 없음).    
- **Parent (부모):** 자식을 가지는 노드.    
- **Child (자식):** 부모에게 연결된 하위 노드.    
- **Leaf (리프):** 자식이 없는 말단 노드.

## BOM(Brower Object Model)
---
브라우저를 제어할 수있도록 모델링한것  
> css를 자바스크립트로 조작 할수 있는 것을 **CSSOM**이라고 한다.

- **DOM**: HTML 문서 구조를 객체로 표현한 모델    
- **BOM (Browser Object Model)**: `window`, `navigator`, `location` 같은 **브라우저 자체**를 제어하는 모델  
    → DOM과 BOM을 함께 사용해 웹페이지 전체를 제어 가능.