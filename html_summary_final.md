# 📗 Do it! HTML 핵심 요약 정리

> 본 문서는 `Do it! HTML+CSS+JavaScript 웹 기본 교과서`를 바탕으로 한 HTML 학습 요약입니다. 
> HTML의 기본 구조부터 주요 태그와 폼 구성까지 실습 중심으로 정리되어 있으며, GitHub 문서 형식에 맞춰 마크다운으로 정리되었습니다.

---

## 📌 목차

1. HTML 문서 구조 및 작성 규칙
2. 시맨틱 구조 태그
3. 텍스트 및 인용 관련 태그
4. 목록 태그
5. 표 관련 태그
6. 이미지 및 미디어 삽입
7. 하이퍼링크 삽입
8. 폼(form)과 입력 요소들

---

## 1. HTML 문서 구조 및 작성 규칙

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8">
    <title>문서 제목</title>
  </head>
  <body>
    <!-- 여기에 본문 내용 작성 -->
  </body>
</html>
```

- `<!DOCTYPE html>`: HTML5 문서임을 선언
- `<html lang="ko">`: 문서 언어 설정
- `<meta charset="UTF-8">`: 문자 인코딩 설정
- `<head>`: 문서의 정보, 메타데이터 포함
- `<title>`: 브라우저 탭에 표시될 제목
- `<body>`: 사용자에게 보여지는 실제 내용

**작성 규칙**
- 태그는 모두 소문자로 작성
- 여는 태그와 닫는 태그 쌍으로 작성 (`<p></p>`, `<div></div>` 등)
- 계층 구조에 따라 들여쓰기 필수
- 속성은 태그 안에 `"속성명="값""` 형식으로 작성

---

## 2. 시맨틱 구조 태그

| 태그 | 설명 |
|------|------|
| `<header>` | 머리말 영역 |
| `<nav>` | 내비게이션 메뉴 영역 |
| `<main>` | 문서의 주요 콘텐츠 |
| `<section>` | 콘텐츠 구역 구분 |
| `<article>` | 독립적인 글이나 콘텐츠 단위 |
| `<aside>` | 보조 콘텐츠 (광고, 사이드바 등) |
| `<footer>` | 바닥글 영역 |
| `<div>` | 의미 없는 블록 레이아웃 용도 (시맨틱 구조는 아님) |
| `<!-- 주석 -->` | 코드에 설명 추가할 때 사용 |

---

## 3. 텍스트 및 인용 관련 태그

### 🔹 구조 강조 태그
| 태그 | 설명 |
|------|------|
| `<h1>`~`<h6>` | 제목 태그 (숫자 작을수록 중요) |
| `<p>` | 문단 |
| `<br>` | 줄바꿈 (닫는 태그 없음) |
| `<hr>` | 수평선 (닫는 태그 없음) |

> 💡 `<br>`은 단순 줄바꿈이고, `<p>`는 문단 전체를 감싸므로 구분해서 사용해야 함.

### 🔹 의미 강조 태그
| 태그 | 설명 |
|------|------|
| `<strong>` | 의미 강조 (굵게 표시, 스크린리더가 강조함) |
| `<b>` | 단순 굵게 (의미 없음, 시각 효과만 있음) |
| `<em>` | 의미 강조 (기울임, 스크린리더가 강조함) |
| `<i>` | 단순 기울임 (의미 없음) |
| `<cite>` | 인용 출처 표시 (책 제목, 기사명 등)

> ✅ `<strong>`과 `<em>`은 스크린리더에서 "중요함"을 강조함. 의미 강조가 필요한 경우 이들을 사용하고, 단순 스타일은 `<b>`, `<i>`를 사용.

### 🔹 기타 텍스트 관련 태그 (요약 설명)
- `<blockquote>`: 인용문
- `<abbr>`: 약어에 마우스오버 설명 추가
- `<code>`: 코드 조각 표시
- `<del>`: 삭제선
- `<ins>`: 삽입선
- `<mark>`: 형광펜 강조
- `<small>`: 작은 글씨
- `<sub>`: 아래 첨자
- `<sup>`: 위 첨자

---

## 4. 목록 태그

```html
<ol>
  <li>순서 있는 항목</li>
</ol>
<ul>
  <li>순서 없는 항목</li>
</ul>
<dl>
  <dt>용어</dt>
  <dd>설명</dd>
</dl>
```

- `<ol>`: 순서 있는 목록 (1, 2, 3…)
- `<ul>`: 순서 없는 목록 (•)
- `<li>`: 각 목록 항목
- `<dl>`: 설명 목록
- `<dt>`: 항목 제목 (Definition Term)
- `<dd>`: 항목 설명 (Definition Description)

---

## 5. 표 관련 태그

```html
<table>
  <caption>표 제목</caption>
  <colgroup>
    <col span="2">
  </colgroup>
  <thead>
    <tr><th>이름</th><th>직업</th></tr>
  </thead>
  <tbody>
    <tr><td>승우</td><td>공대장</td></tr>
  </tbody>
  <tfoot>
    <tr><td colspan="2">총 인원: 1명</td></tr>
  </tfoot>
</table>
```

- `<table>`: 표 전체
- `<caption>`: 표 제목
- `<thead>`, `<tbody>`, `<tfoot>`: 구조 영역 분리
- `<tr>`: 표의 한 행 (row)
- `<th>`: 제목 셀 (굵게, 가운데 정렬)
- `<td>`: 일반 셀
- `rowspan`, `colspan`: 행 또는 열 병합
- `<colgroup>`, `<col>`: 열 단위 스타일 지정

---

## 6. 이미지 및 미디어 삽입

### 📷 이미지 삽입
```html
<img src="이미지.jpg" width="300" height="200" alt="설명글">
```
- `src`: 이미지 파일 경로
- `width`, `height`: 크기 지정
- `alt`: 이미지 대체 텍스트 (스크린리더, 이미지 깨질 때 표시됨)

### 🖼 웹 콘텐츠 설명용 태그
```html
<figure>
  <img src="image.jpg" alt="예시 이미지">
  <figcaption>이미지 설명</figcaption>
</figure>
```
- `<figure>`: 이미지나 미디어 콘텐츠 묶음
- `<figcaption>`: 설명글
- `srcset`, `sizes`: 반응형 이미지 지원 (w 서술자, x 서술자 등)

### 🎵 오디오 / 🎞 비디오 삽입
```html
<audio src="sound.mp3" controls></audio>
<video src="video.mp4" controls width="300" height="200"></video>
```

- 공통 속성: `controls`, `autoplay`, `loop`, `muted`, `preload`, `width`, `height`, `poster`

### 🔌 기타 삽입 방식
- `<object>`, `<embed>`, `<data>`: 외부 콘텐츠 삽입용

---

## 7. 하이퍼링크 삽입

```html
<a href="https://example.com" target="_blank" title="예시 사이트">이동하기</a>
```

- `<a>`: 링크를 생성하는 태그
- `href`: 이동할 주소 지정
- `target="_blank"`: 새 창에서 열기
- `title`: 마우스오버 설명

---

## 8. 폼(form)과 입력 요소들

### 📝 기본 폼 구성
```html
<form method="post" action="/submit">
  <input type="text" name="username">
  <input type="submit" value="제출">
</form>
```
- `method`: `get`은 주소창에 노출, `post`는 보이지 않음
- `action`: 데이터를 보낼 URL
- `target`: 응답 받을 창 지정
- `autocomplete`: 자동완성 on/off

### 🔹 입력 요소 그룹화
```html
<fieldset>
  <legend>회원 정보</legend>
  <label for="user">아이디</label>
  <input type="text" id="user">
</fieldset>
```

### 🔹 input 입력 타입 예시
- 텍스트 입력: `text`, `password`
- 검색/URL/이메일/전화: `search`, `url`, `email`, `tel`
- 체크박스/라디오: `checkbox`, `radio` (속성: `checked`, `value`, `name`)
- 숫자 입력: `number`, `range` (속성: `min`, `max`, `step`, `value`)
- 날짜/시간: `date`, `month`, `week`, `time`, `datetime-local`

### 🔹 전송 관련
- `<input type="submit">`, `<input type="reset">`
- `<button type="submit">`, `<button type="reset">`, `<button type="button">`
- `<input type="image" src="submit.png">`: 이미지 버튼

### 🔹 기타 속성
- `placeholder`: 입력 힌트
- `readonly`: 읽기 전용
- `autofocus`: 자동 커서 포커스
- `required`: 필수 입력

### 📝 여러 줄 입력
```html
<textarea rows="4" cols="50" placeholder="내용 입력"></textarea>
```

### 🔽 드롭다운 목록
```html
<select name="job" size="1" multiple>
  <option value="dev" selected>개발자</option>
  <option value="designer">디자이너</option>
</select>
```

- `<select>`: 드롭다운 박스 (속성: `size`, `multiple`)
- `<option>`: 선택 항목 (속성: `value`, `selected`)

---

이로써 HTML의 주요 태그와 폼 요소에 대한 핵심 요약이 완성되었습니다.
CSS 및 JavaScript 정리는 다음 단계에서 이어집니다. 💪