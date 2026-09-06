# Week 05 — 공개 API 런타임 전환

`serverless-express` 로 돌던 공개 API 람다를 Lambda Web Adapter 로 바꾼
작업의 기록입니다. 바꾼 이유는 하나, 기존 어댑터가 응답을 전부 모은 뒤
반환하는 구조라 SSE 가 구조적으로 불가능했기 때문입니다.

## 보는 방법

HTML 문서라 GitHub 에서는 소스만 보입니다. 아래 링크로 열면 렌더된
화면을 볼 수 있습니다.

- [문서 보기](https://htmlpreview.github.io/?https://raw.githubusercontent.com/GC-Project-Space/ai-luddite/main/members/yeongin-ji/week-05/index.html)
  — 챕터 15개 + 부록. `P` 를 누르면 발표 모드로 바뀝니다.
- [슬라이드 보기](https://htmlpreview.github.io/?https://raw.githubusercontent.com/GC-Project-Space/ai-luddite/main/members/yeongin-ji/week-05/slides.html)
  — 발표용. `←` `→` 로 넘기고 `Esc` 로 전체 보기입니다.

파일을 내려받아 브라우저로 직접 열어도 동일합니다.

## 구성

| 파일 | 내용 |
| --- | --- |
| `index.html` | 전체 문서. 그림 18장이 인라인 SVG 로 들어 있어 외부 의존이 없습니다. |
| `slides.html` | 발표용 슬라이드. reveal.js 를 CDN 에서 받습니다. |
| `figures/` | 그림 원본. 손으로 그린 SVG 16장과 Graphviz 로 뽑은 전체 인프라 지도, 각각의 PNG. |

## 익명화

공개 저장소이므로 [참여 가이드](../../../CONTRIBUTING.md)에 따라 서비스명,
도메인, 티켓 번호는 치환했습니다. 도메인은 전부 `example.com` 계열로
바뀌어 있습니다. 구조, 수치, 판단 근거는 원문 그대로입니다.
