<!-- 01. Hero -->
# 윤우성 · Backend-focused Fullstack Developer

**기술을 선택한 이유를 설명하고, 문제를 직접 검증하며, 과정을 기록으로 남기는 개발자가 되려고 합니다.**
실사용자가 있는 교내 서비스 1건을 운영 중이고, 공모전 플랫폼 1건을 배포까지 끝냈습니다. 둘 다 팀 프로젝트이며 제 담당은 백엔드입니다.

![Java](https://img.shields.io/badge/Java_17-007396?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.5-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Python](https://img.shields.io/badge/Python_3.10-3776AB?style=flat-square&logo=python&logoColor=white) ![Flask](https://img.shields.io/badge/Flask_3-000000?style=flat-square&logo=flask&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

📓 [포트폴리오 (Notion)](https://antique-bangle-481.notion.site/413197909e6b81fcb915ed46d7f33778) · ✉️ wws030816@gmail.com · 한국기술교육대학교 정보통신공학부 3학년 (2028.02 졸업 예정)

---

<!-- 02. Key Highlights -->
## Key Highlights

| | |
|---|---|
| **운영 중인 서비스** | K-OSP — 교내 오픈소스 포털, 2026.02부터 백엔드/프론트 담당·팀장. 실사용자 있음 |
| **배포까지 끝낸 서비스** | FarmLink — 농촌관광 체험 예약·AI 추천 코스, PythonAnywhere 배포 + GitHub Actions 자동 배포 |
| **수상** | 2025 ICT이노베이션 디지털 신기술 공모전 SW개발 부문 **충청권 대상** (FarmLink) · 2026 관광데이터 활용 공모전 예비심사 통과 |
| **기록으로 남은 문제 해결** | 외부 API 401을 가설 배제로 격리(3일) · 캐시 저장소를 메모리/DB/파일 중 근거로 선택 · 정확도 100%의 원인이 데이터 누수임을 진단 |
| **테스트** | FarmLink pytest 773 케이스(770 통과) · K-OSP JUnit 60 클래스 + JaCoCo |

---

<!-- 03. Featured Projects -->
## Featured Projects

<table>
<tr>
<td width="50%" valign="top">

###  K-OSP — 교내 오픈소스 포털
**GitHub 활동을 자동 수집해 랭킹 · 칭호 · 이력서로 바꿔 주는 서비스 (운영 중)**

- **역할** 팀장 · 백엔드/프론트 (개발 2명 중 1) — 칭호 시스템, 시즌 랭킹/티어, 다중 이력서 API, 이력서 PDF·**hwpx 출력**, 학습자료 도메인, 팔로우, Notion 자동기록 CI
- **스택** Java 17 · Spring Boot 3.5 · JPA · PostgreSQL + Flyway · Redis · RabbitMQ / Next.js 15 · TypeScript
- **결정** hwpx는 브라우저가 렌더링하지 못해 백엔드(`hwpxlib`)에서 생성하고 **미리보기는 PDF로 통일** · 시즌 티어는 절대점수가 아닌 **백분위 + 상위 티어만 절대 조건**
- **결과** Flyway 마이그레이션 35건 작성 · BE 33 / FE 58 커밋 (2026.04~09) · PDF 강제 절단 5회 → 0회
- **주의** MSA 구조(RabbitMQ · harvester)는 전임자 설계를 인수해 운영·확장한 것

[Backend README](https://github.com/KOREATECH-OSP/KOSP-Backend) · [Frontend README](https://github.com/KOREATECH-OSP/KOSP-Frontend) · [상세(Notion)](https://antique-bangle-481.notion.site/413197909e6b816f815edac5f4afad72)

</td>
<td width="50%" valign="top">

###  FarmLink — 농촌관광 체험 예약 · AI 추천 코스
**공공 관광 데이터로 체험 전후 코스까지 추천하는 충청권 플랫폼 (2025.09 ~ 2026.09)**

- **역할** 백엔드 (팀 4명 중 BE 2) — TourAPI 4종 연동, 추천 점수·코스 구성, ESG 점수, 조건 카테고리 223개, 파일 캐시, 배포/CI, 팀 규칙 문서
- **스택** Python 3.10 · Flask 3.1 · SQLAlchemy · MySQL · PWA · PythonAnywhere · GitHub Actions
- **결정** 순위는 **규칙 점수**(거리 0.5 · 특산 0.3 · 여석 0.2), LLM은 설명 문장만 — 재현성과 환각 방지 · 외부 API 캐시는 워커가 여럿인 서버라 메모리 대신 **파일**
- **결과** 충청권 대상 · 관광데이터 공모전 예비심사 통과 · pytest 773 케이스 · 본인 커밋 174건
- **한계** PR 규칙을 만들었지만 끝까지 지키지 못함 · 부하 수치 없음

[README](https://github.com/yoonwoosung/SW_id) · [ADR 3건](https://github.com/yoonwoosung/SW_id/tree/develop/docs/adr) · [상세(Notion)](https://antique-bangle-481.notion.site/413197909e6b81268d77f82db26f031f)

</td>
</tr>
</table>

---

<!-- 04. Engineering Decisions -->
## Engineering Decisions — 문제 → 판단 → 결과

**1. 외부 API 401, 3일 (FarmLink)**
문제: 키 오타 · 신청 누락 · 활성화 대기 · 주소 오류가 전부 같은 401. 코딩 도구의 진단도 흔들렸다.
판단: `.env` 키 통일 → 폐기 서버/게이트웨이 공지로 주소 검증 → 코드·환경·환경변수를 다 빼고 **브라우저에서 직접 호출**해 "키 자체가 인증되는가"만 격리 → 서비스단 오류 코드 없는 맨 401 = 게이트웨이 미등록으로 결론.
결과: 코드는 처음부터 맞았고 사흘 뒤 활성화되며 같은 주소에서 95건 수신. 이후 외부 API는 직접 호출로 먼저 격리한다. → [README §3-1](https://github.com/yoonwoosung/SW_id#3-1-tourapi-401--3일-726--729)

**2. 캐시를 메모리도 DB도 아닌 파일에 (FarmLink)**
문제: 추천 코스가 카드마다 관광공사 API를 2~4회 호출해 일일 한도 1,000건이 시연 중 소진.
판단: 메모리 캐시는 PythonAnywhere 워커 수만큼 효과가 나뉘고, DB 캐시는 마이그레이션이 동시 작업 중인 팀원 영역을 건드린다. 파일은 워커가 공유하고 재시작 후에도 남는다. 좌표를 1.1km 격자로 반올림해도 코스가 틀리지 않는 이유까지 커밋 본문에 남겼다.
결과: 한도 소진 재발 없음. 응답시간 개선 폭은 재지 못했다. → [커밋 fad523ca](https://github.com/yoonwoosung/SW_id/commit/fad523ca) · [ADR-0003](https://github.com/yoonwoosung/SW_id/blob/develop/docs/adr/0003-kto-file-cache.md)

**3. 기록 자동화가 기록을 대신하지 못했다 (K-OSP)**
문제: AI 도구로 빠르게 짠 코드가 한 달 뒤 "왜 그렇게 짰는지" 복원이 안 됐다.
판단: 커밋이 올라오면 변경 파일·API·마이그레이션 수를 Notion에 자동 집계하는 CI를 만들었다(7/13). 그런데 54건 중 회고를 직접 적은 건 1건. 8월 공백 뒤 9월부터 **주간 리포트**로 바꿨다 — 도구가 아니라 주기가 문제였다.
결과: 9월 1주~10월 1주 리포트 5부. 그리고 11월, 백엔드 쪽 CI가 7월부터 시크릿 오류로 전부 실패하고 있었음을 발견해 가드를 추가했다. → [K-OSP README §5](https://github.com/KOREATECH-OSP/KOSP-Backend#5-한계와-다시-한다면)

---

<!-- 05. Tech Stack -->
## Tech Stack

| | 실제 배포에 사용 | 수업 · 실습에서 다룸 |
|---|---|---|
| **Backend** | Java 17 · Spring Boot 3.5 · JPA · Flyway / Python 3.10 · Flask 3 · SQLAlchemy | Spring Batch · RabbitMQ(이벤트 흐름 이해) · FastAPI(Cain 예정) |
| **Data** | PostgreSQL · MySQL · Redis(세션 · 잡 큐) · 파일 캐시 설계 | MongoDB · scikit-learn · SQLD 범위(정규화 · 트랜잭션 · 격리수준) |
| **Frontend** | Next.js 15 · React 18 · TypeScript · Tailwind 4 · 바닐라 JS / Jinja · PWA | Flutter(Cain) |
| **Infra** | GitHub Actions(배포 · Notion 자동기록) · PythonAnywhere · AWS Amplify · Docker Compose | GCP(Vertex AI · BigQuery · VM · Cloud Build) · Azure AI 140h · Packet Tracer |
| **External API** | 한국관광공사 TourAPI 4종 · 카카오맵 · 네이버 CLOVA · GitHub API | — |

---

<!-- 06. Additional Experience -->
## Additional Experience

| 프로젝트 | 내용 | 상태 |
|---|---|---|
| [DDoS 탐지 ML](https://github.com/yoonwoosung/MSL) | 머신러닝 과목 팀 프로젝트(팀장). 첫 모델의 테스트 정확도 100%를 성공으로 보지 않고 특성 중요도 1위가 Source IP인 것에서 **데이터 누수**를 진단, 식별자 제거 후 99.79%. 튜닝 128조합으로 기본값이 최적임을 확인 | 완료 (2026-1) |
| [Cain](https://github.com/kang-junhyeong/cain) | AI 다국어 캠퍼스 생활 안내 앱(모바일프로그래밍 팀 프로젝트, 팀장 · 백엔드 담당). Flutter 앱 구조 정리 7커밋. **FastAPI 백엔드는 아직 미구현** | 진행 중 (2026.11~) |
| [Google 테크캠프 GCP 실습](https://github.com/yoonwoosung/GCP-BigQuery-API-Project) | BigQuery API · Sheets 시각화 · Vertex AI AutoML · 인스턴스 그룹 · Cloud Build · RAG 6건을 한 저장소로 통합 | 학습 (2025.07) |

자격·교육: OPIc IH (2026.08) · 전자기능사 · Microsoft AI 엔지니어 과정 140h · Google 테크캠프

---

<!-- 07. Limitations & Next Steps -->
## Limitations & Next Steps

| 한계 | 배운 점 | 다음 행동 |
|---|---|---|
| **부하 수치가 없다.** 테스트·CI는 있지만 응답시간 · 동시 접속을 잰 적이 없다 | "한도 소진을 막았다"는 확인했지만 "얼마나 빨라졌나"는 말할 수 없다 | 다음 프로젝트는 기능보다 먼저 k6로 p50/p95 기준선을 잰다 |
| **팀 규칙을 끝까지 지키지 못했다.** PR 300줄 · 본인 머지 금지를 문서로 정했지만 머지 대부분이 pull 머지, PR 1건 | 규칙은 문서가 아니라 시스템이 지키게 해야 한다 | 브랜치 보호 설정과 CI 게이트부터 건다 |
| **AI 코딩 도구에 의존도가 높다.** 코드의 상당량을 Claude Code로 작성 | 도구의 진단은 흔들린다(401 사례). 결과를 검증하지 않으면 설명할 수 없는 코드가 쌓인다 | 커밋 본문에 원인·대안·검증을 적는 규칙 유지, 핵심 모듈 하나는 도구 없이 다시 짜 본다 |
| **MSA 구조는 내가 설계하지 않았다.** K-OSP의 RabbitMQ · harvester는 전임자 작업 | 인수받은 구조를 운영하며 이벤트 흐름 · 멱등성 · 분산 락 부재를 읽을 수 있게 됐다 | 분산 락(ShedLock) 도입을 다음 이슈로 |

---

<!-- 08. Contact & Links -->
## Contact & Links

- GitHub: [github.com/yoonwoosung](https://github.com/yoonwoosung)
- 포트폴리오(Notion): [antique-bangle-481.notion.site/…](https://antique-bangle-481.notion.site/413197909e6b81fcb915ed46d7f33778)
- 프로젝트 기술 문서: [FarmLink ADR](https://github.com/yoonwoosung/SW_id/tree/develop/docs/adr) · [K-OSP AGENTS.md(코딩 규칙 · 이벤트 흐름)](https://github.com/KOREATECH-OSP/KOSP-Backend/blob/develop/AGENTS.md)
- Email: wws030816@gmail.com
