# 윤우성 — 백엔드 개발자 지망 · 실배포 2건 · 실사용자 서비스 운영 중

> 기능을 만드는 것보다 **왜 그렇게 만들었는지 설명할 수 있는 것**을 목표로 합니다.
> 문제가 생기면 가설을 세우고 하나씩 배제해 원인을 좁히고, 그 과정을 커밋과 문서에 남깁니다.

한국기술교육대학교 정보통신공학부 3학년 · 2028.02 졸업 예정 · 📍 천안 · ✉️ wws030816@gmail.com

---

## 프로젝트

| 프로젝트 | 한 줄 | 역할 | 기간 |
|---|---|---|---|
| **[K-OSP](https://github.com/KOREATECH-OSP/KOSP-Backend)** — 교내 오픈소스 포털 | GitHub 활동을 수집해 랭킹·칭호·이력서로 바꿔 주는 **실사용자 운영 서비스** | 팀장 · 백엔드/프론트 — 칭호 · 시즌 티어 · 다중 이력서 · PDF/hwpx 출력 · 학습자료 · Notion 자동기록 CI | 2026.02 ~ |
| **[FarmLink](https://github.com/yoonwoosung/SW_id)** — 충청권 농촌관광 체험 예약 | 공공 관광 데이터로 체험 전후 **AI 추천 코스**까지 제안 · 공모전 충청권 대상 | 백엔드 — TourAPI 연동 · 추천 점수 · ESG · 파일 캐시 · 배포/CI | 2025.09 ~ 2026.09 |
| **[DDoS 탐지 ML](https://github.com/yoonwoosung/MSL)** — 머신러닝 과목 팀 프로젝트 | 테스트 정확도 **100%의 원인이 데이터 누수**임을 진단하고 제거 → 99.79% | 팀장 · 파이프라인 · 누수 진단 · 모델 비교/튜닝 128조합 | 2026-1학기 |
| [Cain](https://github.com/kang-junhyeong/cain) — AI 다국어 캠퍼스 안내 앱 *(진행 중)* | Flutter + FastAPI 예정 | 팀장 · 백엔드 담당 (현재 Flutter 구조 정리 7커밋, 서버 미구현) | 2026.11 ~ |

## 쓸 수 있는 것

| | 실제로 써서 배포까지 한 것 | 수업·실습에서 다룬 것 |
|---|---|---|
| **백엔드** | Java 17 · Spring Boot 3.5 · JPA · Flyway · Python 3 · Flask 3 · SQLAlchemy | Spring Batch · RabbitMQ(이벤트 흐름 이해) |
| **DB / 캐시** | PostgreSQL · MySQL · Redis(세션·잡 큐) · 파일 캐시 설계 | MongoDB · 정규화/트랜잭션/격리수준(SQLD 응시) |
| **프론트** | Next.js 15 · React 18 · TypeScript · Tailwind 4 · 바닐라 JS/Jinja · PWA | — |
| **인프라 / 운영** | GitHub Actions(배포·Notion 자동기록) · PythonAnywhere · AWS Amplify · Docker Compose | GCP(Vertex AI · BigQuery · VM) · Azure AI 140시간 과정 · Packet Tracer 네트워크 |
| **외부 API** | 한국관광공사 TourAPI 4종 · 카카오맵 · 네이버 CLOVA · GitHub API | — |
| **일하는 방식** | pytest 680 케이스 · JaCoCo · 커밋 컨벤션/ADR 문서 · 회의록 · 주간 리포트 | — |

## 이렇게 일합니다 — 기록이 남아 있는 사례 세 개

**1. 외부 API 401, 3일** — 키 오타·신청 누락·활성화 대기·주소 오류가 전부 같은 401. `.env` 키 통일 → 폐기 서버/게이트웨이 공지로 주소 검증 → 코드·환경·환경변수를 다 빼고 브라우저에서 직접 호출해 "키 자체가 인증되는가"만 격리 → 서비스단 오류 코드 없는 맨 401 = 게이트웨이 미등록으로 결론. 코드는 처음부터 맞았고, 사흘 뒤 활성화되며 같은 주소에서 95건 수신. → [FarmLink README §3-1](https://github.com/yoonwoosung/SW_id#3-1-tourapi-401--3일-726--729)

**2. 캐시를 메모리·DB가 아닌 파일로 둔 이유** — 서버 워커가 여럿이라 메모리 캐시는 워커 수만큼 효과가 나뉘고, DB 캐시는 마이그레이션이 동시 작업 중인 팀원 영역을 건드린다. 그래서 파일. 좌표를 1.1km 격자로 반올림해도 코스가 틀리지 않는 이유까지 커밋 본문에 남김. → [커밋 `fad523ca`](https://github.com/yoonwoosung/SW_id/commit/fad523ca) · [ADR-0003](https://github.com/yoonwoosung/SW_id/blob/develop/docs/adr/0003-kto-file-cache.md)

**3. 기록 자동화가 기록을 대신하지 못했다** — 커밋이 올라오면 변경 파일·API·마이그레이션 수를 Notion에 자동 집계하는 CI를 만들었지만, 54건 중 회고를 직접 적은 건 1건. 8월 공백 뒤 9월부터 주간 리포트로 바꿨다. 도구가 아니라 주기가 문제였다. → [K-OSP README §5](https://github.com/KOREATECH-OSP/KOSP-Backend#5-한계와-다시-한다면)

## 숫자

- 실배포 2건 (PythonAnywhere · AWS Amplify) · 실사용자 있는 서비스 1건 운영 중
- 2025 ICT이노베이션 SW개발 부문 **충청권 대상** · 2026 관광데이터 활용 공모전 **예비심사 통과**
- 2026년 커밋: FarmLink 174 · K-OSP 91 · Flyway 마이그레이션 35건 작성
- OPIc IH (2026.08) · 전자기능사 · Microsoft AI 엔지니어 과정(140h) · Google 테크캠프(GCP/AWS)

## 솔직하게

- 테스트·CI는 있지만 **부하 수치가 없습니다.** 다음 프로젝트에서 가장 먼저 채울 것.
- 팀 규칙(PR 300줄·본인 머지 금지)을 문서로 만들었지만 끝까지 지키지 못했습니다. 다음엔 브랜치 보호 설정부터.
- 코드의 상당량을 AI 코딩 도구로 작성합니다. 그래서 **커밋 본문에 원인·대안·검증을 적는 것**을 규칙으로 두고, 도구의 진단이 흔들릴 때는 도구를 빼고 직접 격리합니다.

---

📓 [포트폴리오(Notion)](https://antique-bangle-481.notion.site/413197909e6b81fcb915ed46d7f33778) · 📄 [FarmLink ADR](https://github.com/yoonwoosung/SW_id/tree/develop/docs/adr) · 🧾 [K-OSP 작업 로그(Notion, CI 자동)](https://app.notion.com/p/39c197909e6b81d49a21c8fca0e62fc6)
