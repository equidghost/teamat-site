# TeamAT 회사소개 사이트 (teamat-site)

현장 업무 관리 서비스 **Workat**을 만드는 회사 **TeamAT**의 소개 사이트입니다.
빌드 과정이 없는 **순수 정적 사이트(HTML/CSS)** 라서, GitHub에 올리고 Vercel에 연결하면 바로 배포됩니다.

## 폴더 구조

```
teamat-site/
├─ index.html        # 메인 페이지 (히어로 · 회사소개 · 서비스 · 브랜드 · 문의)
├─ terms.html        # 이용약관
├─ privacy.html      # 개인정보처리방침
├─ styles.css        # 전체 디자인 (네이비 + 로열블루)
└─ assets/
   ├─ logo-symbol.svg      # A 심볼 (헤더용, 파랑)
   ├─ logo-symbol.png      # A 심볼 PNG (512px)
   ├─ logo-white.svg       # A 심볼 (흰색, 어두운 배경/푸터용)
   ├─ favicon.svg          # 브라우저 탭 아이콘
   └─ apple-touch-icon.png # 모바일 홈화면 아이콘
```

---

## 나중에 언제든 바꾸는 법

### 1) 로고 교체 (가장 쉬움)
**`assets/logo-symbol.svg` 파일만 새 로고로 덮어쓰면** 사이트 전체(헤더·푸터)에 자동 반영됩니다.
HTML은 손대지 않아도 됩니다.
- 진짜 로고 PNG를 쓰고 싶다면: 파일명을 `logo-symbol.png`로 만들어 `assets/`에 넣고,
  `index.html`·`terms.html`·`privacy.html`의 `src="assets/logo-symbol.svg"` → `src="assets/logo-symbol.png"`로만 바꾸세요.
- 어두운 배경(푸터·서비스 카드)용 흰색 버전은 `assets/logo-white.svg`를 교체.
- 탭 아이콘은 `assets/favicon.svg` 교체.

### 2) 글자/문구 교체
`index.html`에서 `<!-- [편집 가능] -->` 주석이 붙은 부분이 바꾸면 좋은 곳입니다.
- 회사 소개 문단: `#about` 섹션
- 이메일/연락처: `#contact` 섹션 (`contact@teamat.kr` → 실제 주소)
- 사업자 정보: `terms.html`, `privacy.html` 하단

### 3) 색상 교체
`styles.css` 맨 위 `:root` 안의 색상 변수만 바꾸면 전체 톤이 바뀝니다.
(`--blue-600` = 포인트 파랑, `--blue-900` = 딥네이비)

---

## 배포 (Vercel)

1. 이 폴더의 **모든 파일**을 GitHub `teamat-site` repo에 업로드
2. Vercel → **Add New Project** → `teamat-site` repo **Import**
3. Framework Preset: **Other** (빌드 설정 없음), 그대로 **Deploy**
4. 배포 후 Project → Settings → **Domains**에서 `teamat.kr` 연결

> ⚠️ 기존 `today-store`(workat.app 운영 앱) 프로젝트는 건드리지 않습니다. 반드시 **새 프로젝트**로 Import 하세요.

---

## 참고
- 로고는 원본 시안을 벡터로 재현한 임시본입니다. 원본 파일이 준비되면 위 "로고 교체" 방법으로 바꾸면 됩니다.
- 약관/개인정보처리방침은 표준 템플릿입니다. 실제 사업 내용에 맞게 검토·수정하세요.
