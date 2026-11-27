# Portfolio — Seohyeon Cho (조서현)

한영 병기 글로벌 K-뷰티 마케터 원페이지 포트폴리오. 단일 HTML 파일이라 그대로 올리면 됩니다.

```
portfolio/
  index.html   ← 사이트 전체 (CSS·JS 포함, 외부 의존성은 Google Fonts 하나뿐)
  README.md    ← 이 파일
```

## 1. 채워 넣을 자리 (플레이스홀더)

`index.html`에서 `[` 로 검색하면 전부 찾을 수 있습니다.

| 위치 | 지금 들어 있는 문구 | 채울 내용 |
|---|---|---|
| Project 01 지표 | `[수치 입력 예: 시딩 00명]` `[수치 입력 예: 000만 뷰]` `[수치 입력 예: ROAS 000%]` | 실제 시딩 인원·조회수·ROAS |
| Project 02 | `[프로젝트명 입력 예정]` `[성과 입력 예: 00명 섭외 / 00만 노출]` | 캠페인명과 성과 |
| Project 03 | `[캠페인명 입력 예정]` `[ROAS · 조회수 입력 예정]` | 캠페인명과 성과 |
| 이미지 자리 | Project 02·03 카드 오른쪽 점선 박스 | 캠페인 비주얼 / 게시물 캡처 |
| 연락처 | `LinkedIn 링크 입력 예정`, `인스타그램 · 틱톡 링크 입력 예정` | 실제 프로필 주소 |

Project 01 카드의 오른쪽은 실제 배포된 가이드(`menokin-lift-guide.netlify.app`)의 미니 커버를 CSS로 그려 둔 것입니다. 링크는 이미 연결되어 있습니다.

## 2. 수정 방법

### 숫자·문구 바꾸기
`index.html`에서 해당 문구를 찾아 그대로 바꾸면 됩니다. 각 문구는 `data-kr="..."` `data-en="..."` 두 언어를 함께 갖고 있으니 **양쪽 다** 바꿔 주세요.

### 이미지 넣기
점선 박스를 이미지로 교체합니다.

```html
<!-- before -->
<div class="visual-placeholder"> ... </div>

<!-- after -->
<img src="images/project-02.jpg" alt="Japan seeding campaign" style="width:100%;border-radius:16px;" />
```
이미지는 `portfolio/images/` 폴더를 만들어 함께 올리면 됩니다.

### 링크 넣기
`<span class="proj-link" style="...">` 를 `<a class="proj-link" href="https://..." target="_blank" rel="noopener">` 로 바꾸고 회색 인라인 스타일을 지우면 활성 링크처럼 보입니다.

## 3. 언어 전환

- 오른쪽 위 **KR / EN** 버튼으로 전체 문구가 바뀝니다.
- 기본값은 한국어(`lang="ko"`)입니다.
- 기본값을 영어로 두고 싶으면 `<script>` 안의 `apply()` 호출에 `apply('en');`을 한 줄 추가하세요.

## 4. 배포

### Netlify (가장 빠름)
1. https://app.netlify.com/drop 접속
2. `portfolio` 폴더를 그대로 드래그
3. 발급되는 `xxx.netlify.app` 주소 사용 (원하면 Site settings → Change site name)

### GitHub Pages
1. 저장소에 `portfolio` 폴더의 `index.html`을 올림 (루트에 두거나 `/docs` 폴더 사용)
2. Settings → Pages → Branch/폴더 선택 → 저장
3. `https://<아이디>.github.io/<저장소>/` 로 열림

두 경우 모두 빌드 과정이 필요 없습니다.

## 5. 참고

- 폰트: Google Fonts(Poppins · Inter · Noto Sans KR)만 외부에서 불러옵니다. 오프라인에서도 열리지만 폰트는 기본 글꼴로 대체됩니다.
- 반응형: 1440 / 1280 / 1024 / 820 / 768 / 390px에서 가로 스크롤 없이 확인했습니다.
- 인쇄(PDF 저장) 시에도 레이아웃이 깨지지 않습니다.
