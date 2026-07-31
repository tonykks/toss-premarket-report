# toss-premarket-report

공개 시장·뉴스 기반 **장전 시장분석 보고서** HTML만 담는 public 저장소입니다.

- 본체 운용 코드·Toss API·계좌/보유/주문·DB·Secret은 **포함하지 않습니다**.
- 생성·분석 파이프라인은 private 저장소(`Toss_Invest_Agent`)에서만 실행됩니다.
- 이 저장소에는 Live 성공 시 갱신되는 **최신 `docs/index.html`** 만 반영됩니다.

## 고정 URL (GitHub Pages)

| 용도 | URL |
|------|-----|
| 매일 보는 주소 | https://tonykks.github.io/toss-premarket-report/ |
| 탭 | `#summary` · `#today` · `#analysis` · `#evidence` |

예: https://tonykks.github.io/toss-premarket-report/#today

## Pages 설정

1. Settings → Pages
2. Source: **Deploy from a branch**
3. Branch: **`main`** · Folder: **`/docs`**

## 포함 / 제외

**포함**

- `docs/index.html` — 최신 장전 보고서 (단일 진입점)
- `.nojekyll` — Jekyll 처리 생략
- `README.md` — 이 안내

**제외**

- Toss Open API / Flask / DB / `.env` / `data/**`
- Gemini API key 및 기타 credential
- 계좌·보유·평단·주문·실현손익
- 파이프라인 소스·테스트·워크플로·archive markdown

## 동기화

private 저장소의 `premarket-github` 워크플로가 Live 성공 후
`docs/premarket/index.html`을 이 저장소 `docs/index.html`로 push합니다.
Deploy token/Secret은 **public 저장소에 두지 않습니다** (private repo Secret만 사용).

## 면책

본 보고서는 공개 자료 기반의 참고용 시장 분석이며, 매수·매도 지시나 투자 권유가 아닙니다.
