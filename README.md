# 🌕 달님 변환기 (lunar-converter)

양력 ↔ 음력 변환 웹 도구. 윤달·간지·띠·설날/추석 디데이 지원.
GitHub Pages로 배포해서 블로그에 iframe으로 임베드하는 용도.

## 파일 구성

| 파일 | 역할 |
|---|---|
| `index.html` | 소개 랜딩 페이지 (히어로 + 툴 임베드 + 기능 소개 + SEO 아티클) |
| `converter.html` | 변환기 본체 — **완전 싱글 파일** (음력 데이터 라이브러리 인라인 내장). 이 파일 하나만 있으면 어디서든 동작 |
| `klc.min.js` | 음력 데이터 원본 라이브러리 ([korean-lunar-calendar](https://www.npmjs.com/package/korean-lunar-calendar), MIT). converter.html에 인라인된 것과 동일 — 업데이트 참고용 |

## 기능

- 양력 → 음력 / 음력 → 양력 양방향 변환
- 윤달(閏月) 완벽 지원 (입력 시 윤달 체크박스)
- 육십갑자(을사년 등) + 십이지 띠 표시
- 오늘의 음력 · 다음 설날/추석 D-day 자동 표시
- 서기 1000년 ~ 2050년 커버 (한국천문연구원 기준 데이터)
- 모바일 반응형

## 배포 (GitHub Pages)

```bash
cd lunar-converter
git init
git add .
git commit -m "🌕 음력 양력 변환기 초기 배포"
git branch -M main
git remote add origin https://github.com/seunglover/lunar-converter.git
git push -u origin main
```

그 후 GitHub 리포지토리 → **Settings → Pages → Branch: main / (root)** 선택.
몇 분 뒤 `https://seunglover.github.io/lunar-converter/` 에서 접속 가능.

## 블로그 임베드

티스토리/네이버 블로그 글쓰기 HTML 모드에:

```html
<iframe src="https://seunglover.github.io/lunar-converter/converter.html"
        width="100%" height="680" frameborder="0"
        style="border-radius:16px"></iframe>
```

## 배포 전 할 일

- [x] `index.html` 안의 `seunglover` 2곳을 실제 GitHub 아이디로 교체 (nav 링크, footer 링크)
- [x] 임베드 코드 블록의 `seunglover`도 교체

## 라이선스

코드: 마음대로 사용. 음력 데이터 라이브러리: MIT (korean-lunar-calendar).
