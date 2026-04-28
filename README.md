# openclaw-webinar-summary (SOPA5 운영본)

오픈클로 / 뽀짝이의 서재 웨비나 부가 자료(녹화본 보충, 핵심 자료집 PDF 등)를 호스팅하는 정적 사이트.
Vercel(`sopa5s-projects` 팀, alias `openclaw-webinar-summary-wine.vercel.app`)이 `public/`을 자동 배포한다.

원래는 [`cpuxp11/openclaw-webinar-summary`](https://github.com/cpuxp11/openclaw-webinar-summary) (병찬님 운영) 의 fork였으나, 2026-04-25부터 **SOPA5(소파님) 단독 운영본**으로 분리해 머지·승인 절차 없이 즉시 배포할 수 있도록 전환했다. 두 레포는 더 이상 동기화되지 않는다.

## 디렉토리 구조

```
public/
├── index.html                       # 4/14 회차 — 오픈클로 멀티에이전트 협업 가이드 (legacy)
├── frames/                          # 4/14 회차 슬라이드 캡처
└── 2026-MM-DD-{speakerSlug}/
    └── <자료명>.pdf                  # 회차별 자료집
```

## 회차별 자료 추가 워크플로우

1. 새 회차 폴더 생성 (예: `public/2026-04-21-giacomo/`)
2. PDF/이미지 등 자료 파일 추가
3. main 브랜치에 직접 commit + push
4. Vercel 자동 배포 → `https://openclaw-webinar-summary-wine.vercel.app/<폴더>/<파일>` 즉시 활성

## 호스팅 정책

- main 브랜치 = 운영. PR/리뷰 없이 직접 push 허용 (단독 운영).
- 자료집 등 PDF는 5MB 미만 권장. 그 이상은 LFS 또는 외부 CDN 검토.
- 웨비나 후기 리워드 이메일(`webinar-judge-send` 스킬)에서 이 도메인의 URL을 그대로 인용.

## 회차별 자료 (현재까지)

| 회차 | 슬러그 | 자료 |
|------|--------|------|
| 4/21(화) — Hermes vs OpenClaw / Giacomo님 | `2026-04-21-giacomo` | `hermes-vs-openclaw.pdf` |
| 4/14 (legacy, 통합 페이지) | `index.html` + `frames/` | 멀티에이전트 협업 가이드 |
