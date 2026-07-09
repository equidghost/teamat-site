# TeamAT 회사소개 사이트 (teamat-site)

현장 업무 관리 서비스 **Workat**을 만드는 회사 **TeamAT**의 소개 사이트입니다.
빌드 과정이 없는 **순수 정적 사이트(HTML/CSS)** 라서, GitHub에 올리고 Vercel에 연결하면 바로 배포됩니다.

## 폴더 구조

```
teamat-site/
├─ index.html        # 메인 페이지 (히어로 · 회사소개 · 서비스 · 브랜드 · 문의)
├─ terms.html        # 이용약관
├─ privacy.html      # 개인정보처리방침
├─ account-deletion.html # 계정·데이터 삭제 안내
├─ 404.html          # Not Found 페이지
├─ styles.css        # 전체 디자인 (네이비 + 로열블루)
├─ vercel.json       # Vercel clean URL / 보안 헤더 설정
├─ robots.txt
├─ sitemap.xml
├─ logo-*.png        # TeamAT / Workat 로고
├─ og-image.png
├─ favicon.svg
├─ apple-touch-icon.png
├─ teamat-clouds.png # 히어로 구름 애니메이션 배경
└─ teamat-cloud-animation-preview.html # 히어로 애니메이션 시안
```

---

## 나중에 언제든 바꾸는 법

### 1) 로고 교체 (가장 쉬움)
이 사이트는 배포 루트에 모든 파일을 두는 **flat 구조**입니다. `assets/` 폴더로 옮기면 배포 경로가 깨질 수 있습니다.
- 헤더 로고: `logo-teamat.png`
- 푸터 로고: `logo-teamat-white.png`
- Workat 로고: `logo-workat.png`, `logo-workat-mark.png`
- 탭 아이콘: `favicon.svg`
- 모바일 홈화면 아이콘: `apple-touch-icon.png`

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
