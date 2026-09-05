### 이헌준

고려대학교 컴퓨터학과. 궁금한 건 일단 끝까지 만들어보는 편입니다.

[블로그](https://bhj2837.github.io) · [자세한 소개](https://bhj2837.github.io/about/) · [rex2837@korea.ac.kr](mailto:rex2837@korea.ac.kr)

<br>

```
Language   Java · Python · C/C++ · JavaScript
Frontend   Next.js 14 · Vue 3 · TailwindCSS
Backend    Django 5 / DRF · Crow (C++) · Paper API
ML/NLP     PyTorch · HuggingFace Transformers
Infra      GCP · Vercel · Railway
```

<br>

### Projects

**[LearningPath](https://github.com/bhj2837/learningpath)** — AI 학습 로드맵 생성 플랫폼
`Next.js 14` `Django 5` `Claude API`
남의 리소스 ID 로 접근하면 존재 여부조차 흘리지 않도록 404 를 반환합니다.
IDOR·인증·입력 검증 회귀 테스트 34개.

**[SharedFate](https://github.com/bhj2837/sharedfate)** — 운명 공유 마인크래프트 플러그인
`Java 21` `Paper API` `GCP`
데미지·인벤토리·죽음을 공유합니다. 다만 전부 공유하면 아무도 자기 장비를 못 챙겨서,
인벤토리는 슬롯 9–35 만 공유하고 핫바·갑옷은 개인 소유로 남겼습니다.

**[schedule-engine](https://github.com/bhj2837/schedule-engine)** — C++ 일정 최적화 서버
`C++17` `Crow`
`score = deadline - priority × 3600` — 우선순위 한 단계를 마감 한 시간으로 환산해
EDF 에 섞었습니다. API 와 대시보드를 exe 하나에서 서빙합니다.

**[mini-shell](https://github.com/bhj2837/mini-shell)** — C 로 만든 UNIX 셸
`C` `POSIX`
파이프·리다이렉션·백그라운드 실행·시그널 처리를 직접 구현. `Ctrl+C` 는 셸이 아니라
포그라운드 작업만 죽입니다.

**[korean-dialogue-generation](https://github.com/bhj2837/korean-dialogue-generation)** — 한국어 멀티턴 대화 생성
`PyTorch` `KoBART`
`<P01>` / `<P02>` 화자 토큰을 추가해 멀티턴 맥락에서 발화 주체를 구분하도록 했습니다.

**[daily-brief](https://daily-brief-neon-three.vercel.app)** — 개인 대시보드
`Vue 3`
날씨·일정·뉴스를 한 화면에. 이전 weather 프로젝트를 컴포넌트로 떼어 재사용했습니다.
