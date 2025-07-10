# 📗 Do it! HTML 헌신 요조 정리

> 본 문서는 `Do it! HTML+CSS+JavaScript 웹 기본 교과서`를 방해한 HTML 학습 요조입니다.\
> 실작 중심으로 구성되어 있으며, 직접 코드 작성과 함꿐 정리한 내용입니다.

---

## 📌 목차

1. HTML 문서 구조
2. 텍스트 태그
3. 링크/이미지
4. 목록
5. 폼 (uc785력 양식)
6. **표 (**\`\`**)**
7. **멀티미디어 (**`**, **`**, ****\`\`****)**
8. **기타 시멘트 태그**
9. 마무리 메모

---

## 1. HTML 문서 구조

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <title>문서 제목</title>
  </head>
  <body>
    <!-- 여기서부터 불음 내용 작성 -->
  </body>
</html>
```

- `<!DOCTYPE html>`: HTML5 문서임을 선언
- `<html>`: HTML 문서의 루트 요소
- `<head>`: 문서 정보 (제목, 인코딩, 외부 리소스 등)
- `<body>`: 사용자에게 보여진는 내용

---

## 2. 텍스트 관련 태그

| 태그               | 의미                   |
| ---------------- | -------------------- |
| `<h1>` \~ `<h6>` | 제목 (숫자가 작을수록 크고 중요함) |
| `<p>`            | 문단                   |
| `<br>`           | 줄바꿀기 (닫는 태그 없음)      |
| `<hr>`           | 수평선 (닫는 태그 없음)       |
| `<strong>`       | 강조 (굵어진 글씨, 의미 강조)   |
| `<em>`           | 강조 (기울임, 것지개 강조)     |
| `<span>`         | 인라인 영역 지정 (스타일링용)    |
| `<div>`          | 블록 영역 지정 (레이아웃용)     |

---

## 3. 링크와 이미지

```html
<a href="https://example.com">링크 텍스트</a>
<img src="cat.jpg" alt="고양이 사진" />
```

- `<a>`: 하이퍼리크
- `<img>`: 이미지 삽입 (`alt`는 대체 텍스트)

---

## 4. 목록 태그

```html
<ul>
  <li>순서 없는 항목</li>
</ul>

<ol>
  <li>순서 있는 항목</li>
</ol>
```

- `<ul>`: 순서 없는 리스트 (\u2022)
- `<ol>`: 순서 있는 리스트 (1, 2, 3)
- `<li>`: 리스트 항목

---

## 5. 폼 기본

```html
<form>
  <input type="text" />
  <input type="submit" value="제출" />
</form>
```

- 사용자로부터 데이터를 입력받는 요소
- `<input>`, `<textarea>`, `<select>` 등 다양한 입력 유형 존재

---

## 6. 표 관련 태그

```html
<table>
  <thead>
    <tr><th>이름</th><th>직업</th></tr>
  </thead>
  <tbody>
    <tr><td>승우</td><td>공대장</td></tr>
    <tr><td>진우</td><td>용백</td></tr>
  </tbody>
</table>
```

| 태그        | 설명                |
| --------- | ----------------- |
| `<table>` | 표 전체를 감사는 태그      |
| `<thead>` | 표의 머리글 부분         |
| `<tbody>` | 표의 보문 데이터         |
| `<tr>`    | 행(Row)            |
| `<th>`    | 제목 셀 (굵게, 가운데 정렬) |
| `<td>`    | 일반 셀              |

> 💡 `colspan`, `rowspan`으로 열/행 병합 가능

---

## 7. 멀티미디어 태그

### 🔊 오디오

```html
<audio controls>
  <source src="sound.mp3" type="audio/mpeg" />
  브라우저가 audio 태그를 지원하지 않습니다.
</audio>
```

### 🎞 비디오

```html
<video controls width="300">
  <source src="video.mp4" type="video/mp4" />
  브라우저가 video 태그를 지원하지 않습니다.
</video>
```

### 🌐 외부 컨틸애시 삽입 (iframe)

```html
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/영상ID"
  frameborder="0" allowfullscreen>
</iframe>
```

---

## 8. 시멘트(의미 기반) 태그

| 태그          | 용도                |
| ----------- | ----------------- |
| `<header>`  | 페이지 또는 세트의 머리말    |
| `<nav>`     | 네비가션 링크 영역        |
| `<main>`    | 주요 콘텐츠 영역         |
| `<section>` | 구분된 콘텐츠 무기        |
| `<article>` | 독립적인 글, 포스트       |
| `<aside>`   | 부가 콘텐츠 (광고, 사이드바) |
| `<footer>`  | 페이지나 글의 바닥글       |

> ✅ HTML5에서는 시멘트 태그를 활용해 **접근성과 구조 명확성**을 높이는 것이 중요함

---

## 9. 마무리 개인 메모 ✨

- `<div>` vs 시멘트 태그:

  - `div`는 구조를 나누기 위한 용도
  - `section`, `article`등은 **의미까지 함께 전달**함

- `<iframe>`은 **외부 컨틸애시 삽입**할 때 사용되지만\
  보안 및 성능 유의점이 있어 **필요한 경우만** 사용 권장

---

## 📁 저장 및 활용 핀

- 이 파일을 `README.md` 또는 `html-summary.md`로 저장
- GitHub에 업로드하면 자동 렌더링되어 문서처럼 확인 가능
- 실제 프로젝트에 쓰는 예시나 코드 시넓은 `code/` 포버에 다루고, 이미지는 `images/` 포버로 관리 권장

---

## ✅ 다음 계획 (html-css-js 정리 환경)

| 파트         | 상태    | 비고              |
| ---------- | ----- | --------------- |
| HTML 기본    | ✅ 완료  | 지금 이 내용         |
| CSS        | ⏳ 예정  | 선택자, 속성, 박스모델 등 |
| JavaScript | 🔜 이후 | 변수, 이벤트, DOM 등  |

---

