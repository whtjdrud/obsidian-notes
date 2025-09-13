

```html
<body>

```
- `<body>` 실제 화면 요소 시작
- `<div class="app">` 앱전체 컨테이너
	- 그리드 레이아웃 적용
	- 사이드바, 본문 영역 배치의 기준점
	- 즉 화면을 크게 좌측(사이드바) / 우측(본문) 구조로 구분

### 사이드바
```html
<aside id="sidebar" class="sidebar">
```
- `<aside>` 문서의 보조 영역을 의미하는 시맨틱 태그
- 메인 콘텐츠는 아니지만 탐색, 관리 필수영역 
	- `id="sidebar`는 JS에서의 고유 식별자
	- `class="sidebar"` css 스타일 적용
	- **id = 유일한 식별 / class 공통 규칙**

## inner
---
```html
<aside id="sidebar" class="sidebar">
	<div class="inner">
	</div>
</aside>
```
- 사이드 바 안의 내부 래퍼
- 사이드 바 안의 영역(컨텐츠)를 **스크롤 가능한 영역으로 묶기 위함** 
- CSS에서 PADDING + OVERFLOW 규칙 적용
	- **사이드바 내용 많아질 때 스크롤바 생성**

```html
<button id="collapseBtn" class="collapse-btn" title="Collapse">
 <<
</button>
```
- 사이드바 토글 버튼 (접기 / 펼치기)
- id > JS 이벤트 연결
- CLASS > 버튼 스타일 적용
- TITLE > 마우스 오버 시 툴팁(접근성강화 )

![](Pasted%20image%2020250913205621.png)


##  USER-BOX
---
- 사용자 정보 박스
- 아바타, 이름, 이메일 한 덩어리그룹화 
- 사이드바 상단에 계정 정보 표시
```html
<!-- User -->
<div class="user-box">
	<div class="avater">/</div>
	<div class="user-meta">
		<strong>Guest</strong>
		<small>guest@example.com</small>
	</div>
</div>
```

