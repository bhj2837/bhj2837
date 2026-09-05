<div align="center">


풀스택 웹 · C/C++ 시스템 프로그래밍 · 딥러닝

[![Blog](https://img.shields.io/badge/Blog-bhj2837.github.io-181717?style=flat-square&logo=github&logoColor=white)](https://bhj2837.github.io)
[![Portfolio](https://img.shields.io/badge/Portfolio-About-0A66C2?style=flat-square)](https://bhj2837.github.io/about/)
[![Email](https://img.shields.io/badge/rex2837@korea.ac.kr-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:rex2837@korea.ac.kr)

</div>

<br>

## Skills

| | |
|---|---|
| **Language** | `Java` `Python` `C` `C++17` `JavaScript` |
| **Frontend** | `Next.js 14` `Vue 3` `TailwindCSS` `Vite` |
| **Backend** | `Django 5 / DRF` `Crow (C++)` |
| **ML / NLP** | `PyTorch` `HuggingFace` `KoBART` `LSTM` |
| **Infra** | `GCP` `Vercel` `Railway` `Docker` `CMake` |

<br>

## Projects

### [LearningPath](https://github.com/bhj2837/learningpath) — AI 학습 로드맵 생성 플랫폼

`Next.js 14` `Django 5` `DRF` `Claude API` · 2026.02 – 2026.09

목표·기간·수준을 입력하면 주차별 커리큘럼과 추천 자료, 체크리스트를 생성합니다.
가장 오래 붙잡은 건 AI 가 아니라 **권한**이었습니다.

- 모든 ViewSet 의 `get_queryset()` 을 요청자 기준으로 좁혀 IDOR 을 구조적으로 차단
- 남의 리소스 ID 로 조회하면 `403` 이 아닌 **`404`** — 존재 여부조차 흘리지 않기 위해
- IDOR · 인증 · 입력 검증 · 저장 회귀를 포함한 **테스트 34개**
- 중첩 직렬화로 생긴 N+1 을 `prefetch_related` 로 해소, 생성 API 는 시간당 10회 스로틀

<br>

### [schedule-engine](https://github.com/bhj2837/schedule-engine) — C++ 일정 최적화 서버

`C++17` `Crow` `CMake` · 2026.02

EDF 는 마감일만 보기 때문에 마감이 먼 중요한 일이 계속 밀립니다.
우선순위를 **시간 단위로 환산**해 하나의 점수로 합쳤습니다.

```cpp
score = deadline - (priority * 3600);   // 낮을수록 먼저
```

가중치를 곱하는 대신 같은 차원(초)으로 바꿔 빼는 게 핵심이었습니다.
REST API 와 간트 차트 대시보드를 **exe 하나에서 함께 서빙**해 빌드 결과만 옮기면 동작합니다.

<br>

### [mini-shell](https://github.com/bhj2837/mini-shell) — C 로 만든 UNIX 셸

`C` `POSIX` · 2026.03

파서 · 실행기 · 내장 명령어를 직접 작성. 파이프라인, 입출력·추가 리다이렉션,
백그라운드 실행, `cd -`, `export`, 시그널 처리를 지원합니다.
손으로 짜면서 파이프라인이 결국 **자식마다 `dup2` 로 fd 를 갈아끼우는 일**이라는 것과,
`Ctrl+C` 가 셸까지 죽지 않게 하려면 포그라운드 작업을 따로 다뤄야 한다는 걸 알았습니다.

<br>

### [daily-brief](https://daily-brief-neon-three.vercel.app) — Vue 3 정보 포털

`Vue 3` `Vue Router` `Vite` · 2026.08 · SK AX SKALA 종합과제

뉴스·날씨·환율·코인·증시·게시판까지 **15개 라우트**, 전 화면 Lazy Loading,
글쓰기에는 `beforeEach` 인증 가드. 외부 API 7종을 붙이면서 **키가 없으면 Mock 으로
자동 폴백**하도록 만들어, 심사자가 키 발급 없이도 전체 기능을 볼 수 있게 했습니다.

<br>

### [korean-dialogue-generation](https://github.com/bhj2837/korean-dialogue-generation) — 한국어 멀티턴 대화 생성

`PyTorch` `HuggingFace` `KoBART` · 2024 · 자연어처리 최종 프로젝트

멀티턴을 한 줄로 이어 붙이면 모델이 누가 한 말인지 구분하지 못합니다.
`<P01>` / `<P02>` 화자 토큰을 토크나이저에 추가하고 임베딩을 확장해 해결했습니다.
SNS 데이터라 초성 반복 정규화 등 전처리 비중이 컸습니다.

<br>

## Coursework

- **COSE471 데이터 과학** — [Sign-Language-Translation](https://github.com/bhj2837/Sign-Language-Translation)
  LSTM 으로 수어 시퀀스를 학습하고 웹캠 입력을 받아 실시간 추론까지 구현
- **COSE474 딥러닝** — [강의 실습 및 최종 프로젝트](https://github.com/bhj2837/20242R0136COSE47402)

<br>

## Writing

[**bhj2837.github.io**](https://bhj2837.github.io) — 알고리즘 설계 기법을 교재 순서대로
정리합니다. 완전 탐색부터 감소 정복 · 분할 정복 · 변환 정복까지, 답이 아니라
*왜 그 접근이 나오는지* 를 남기는 게 목적입니다.
