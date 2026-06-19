<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=메일상자&fontSize=80&fontColor=ffffff&animation=twinkling&fontAlignY=38&desc=AI%20기반%20다중%20계정%20메일%20인박스%20자동화%20서비스&descAlignY=62&descSize=20&descColor=d0e8ff" />

<br/>

[![GitHub org](https://img.shields.io/badge/GitHub-mailsangja-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/mailsangja)
&nbsp;
[![AJOU](https://img.shields.io/badge/AJOU%20SOFTCON-2026--1-0057A8?style=flat-square&logo=academia&logoColor=white)](https://softcon.ajou.ac.kr/works/works.asp?uid=2298)
&nbsp;
![MAU](https://img.shields.io/badge/MAU-200%2B-brightgreen?style=flat-square&logo=googlegmail&logoColor=white)
&nbsp;
![Service](https://img.shields.io/badge/Service-Live-success?style=flat-square&logo=vercel&logoColor=white)
&nbsp;

<br/>

> **여러 Gmail 계정, 이제 하나로 관리하세요.**  
> AI가 라벨을 분류하고, RAG가 맞춤 답장 초안을 작성해드립니다.

<br/>

[메일상자 시연영상](https://github.com/user-attachments/assets/7380cda4-5d05-4051-b72e-4b2b220c378f)

[![Service](https://img.shields.io/badge/🌐%20서비스%20바로가기-mail.ajou.app-4A90E2?style=for-the-badge)](https://mail.ajou.app/)

</div>

---

## 🏆 수상 내역

<div align="center">

| 시상식 | 수상 | 날짜 |
|:---:|:---:|:---:|
| 🥉 아주대학교 **SOFTCON 2026-1** | **장려상 (3등)** | 2026.06.11 |
| 🌟 아주대학교 **SOFTCON 2026-1** | **인기상** | 2026.06.11 |

> **SOFTCON** — 아주대학교 소프트웨어학과 졸업작품 전시회  
> [SOFTCON 2026-1 작품 페이지](https://softcon.ajou.ac.kr/works/works.asp?uid=2298)

</div>

---

## 🔥 서비스 개요

메일상자는 여러 Gmail 계정을 하나의 인박스에서 통합 관리하고, AI 기반 자동 라벨링과 RAG 기반 답장 초안 생성을 제공하는 메일 관리 자동화 서비스입니다.

사용자는 여러 계정을 오가며 메일을 확인할 필요 없이 하나의 화면에서 메일을 조회할 수 있으며, AI가 메일의 성격을 분석해 라벨을 제안하고 중요 메일 관리, 필터링, 알림 설정, 민감정보 관리까지 연결할 수 있습니다.

<table>
  <tr>
    <th align="center" width="100">구분</th>
    <th>내용</th>
  </tr>
  <tr>
    <td align="center">🎯 <b>Target</b></td>
    <td>여러 Gmail 계정을 동시에 관리해야 하는 사용자</td>
  </tr>
  <tr>
    <td align="center">😣 <b>Problem</b></td>
    <td>빠른 인박스 전환의 어려움 &nbsp;·&nbsp; 중요 메일 누락 &nbsp;·&nbsp; AI 환경설정 비용 부담 &nbsp;·&nbsp; 메일 관리 효율성 저하</td>
  </tr>
  <tr>
    <td align="center">✅ <b>Solution</b></td>
    <td><b>다중 계정 인박스</b> + <b>AI 자동 라벨링</b> + <b>AI 자동 답장</b></td>
  </tr>
  <tr>
    <td align="center">💡 <b>POD</b></td>
    <td>다중 계정·벤더 통합 인박스, RAG·LLM 기반 개인화 메일 분류·작성 자동화</td>
  </tr>
</table>

---

## 🚀 핵심 기능 (서비스 상세 소개)

### 📥 다중 Gmail 계정 통합 인박스

여러 Gmail 계정을 하나의 화면에서 조회할 수 있는 통합 인박스를 제공합니다.  
사용자는 계정을 반복해서 전환하지 않아도 전체 메일 흐름을 한 번에 확인할 수 있습니다.

- Gmail OAuth 기반 계정 연동 (서비스 로그인과 별도로 인박스 접근 권한 확보)
- 계정별 메일 동기화 및 통합 조회
- 메일 계정 단위 필터링 및 검색 지원
- Thread 단위 메일 묶음 보기

### 🏷️ AI 기반 자동 라벨링

메일 제목, 본문, 발신자 정보를 기반으로 AI가 적절한 라벨을 자동 제안합니다.  
제안된 라벨은 필터링, 알림 설정, 민감정보 관리 정책과 연결하여 메일 관리 자동화의 기준으로 활용할 수 있습니다.

- LLM 기반 메일 내용 분석 후 라벨 자동 추천
- 사용자 정의 라벨 + 라벨 그룹 관리
- 라벨 기반 필터링 및 실시간 알림 정책 연동
- 과거 메일 일괄 재분류 (Debounce + Rate Limit 제어)

### ✉️ RAG 기반 맞춤 답장 초안 생성

사용자의 기존 메일 작성 패턴을 벡터화하고, 유사한 메일 맥락을 검색하여 개인화된 답장 초안을 생성합니다.

- 사용자 메일 패턴 기반 임베딩 → pgvector 저장
- 유사 메일 검색 기반 RAG 구성
- 대화 맥락을 반영한 답장 초안 생성 및 검토
- 2~3개 답장 옵션 제안 → 편집기에서 자유 수정 후 발송

### ✍️ AI 보조 메일 작성

- 프롬프트 입력 → AI가 메일 제목·본문 초안 생성
- 전송 전 AI 자동 리뷰: 오타, 첨부 누락, 맥락 적절성 팝업 알림

### ⚡ 실시간 메일 동기화 및 비동기 처리

Google Pub/Sub과 Gmail API를 통해 신규 메일 이벤트를 수신하고, RabbitMQ 기반 비동기 처리 구조로 메일 저장, 라벨링, 알림 작업을 안정적으로 분리했습니다.

- Google Pub/Sub 기반 Gmail 변경 이벤트 수신
- RabbitMQ 기반 비동기 메일 처리 (Direct Exchange + DLX)
- Backpressure 적용을 통한 트래픽 급증 대응
- DLQ 및 Dead Letter Alert 기반 실패 메시지 추적
- FCM(Firebase Cloud Messaging) 기반 실시간 Push 알림

### 💳 구독 및 결제

- Portone 연동 결제 시스템
- 플랜별 AI 기능 사용 제한 및 Rate Limit 관리

---

## 🏗️ 설계 및 구현

### Repository 구조

| 레포지토리 | 역할 | 기술 |
|:---|:---|:---|
| [`mailsangja/docs4capstone`](https://github.com/mailsangja/docs4capstone) | User Story 이슈 관리, 기획 문서 | GitHub Projects |
| [`mailsangja/mailsangja-server`](https://github.com/mailsangja/mailsangja-server) | 백엔드 서버 (core + worker + db 멀티모듈) | Spring Boot 4 / Java 21 |
| [`mailsangja/mailsangja-frontend`](https://github.com/mailsangja/mailsangja-frontend) | 프론트엔드 웹 앱 | React 19 / TypeScript / Vite |
| [`mailsangja/mailsangja-infra`](https://github.com/mailsangja/mailsangja-infra) | k3s 클러스터 GitOps 매니페스트 및 Argo CD 배포 구성 | Kubernetes / Argo CD / Sealed Secrets |

> 자세한 설계, 모듈 구조, CI/CD, 협업 방식은 [`docs4capstone` README](https://github.com/mailsangja/docs4capstone)를 참고하세요.

---

### 핵심 기술 스택

<div align="center">

**Backend**

![Spring](https://img.shields.io/badge/Spring_Boot_4-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Java](https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_+_pgvector-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Shadcn/ui](https://img.shields.io/badge/shadcn/ui-000000?style=for-the-badge&logo=shadcnui&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

**Infra / DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Argo CD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Grafana_Loki-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Tempo](https://img.shields.io/badge/Grafana_Tempo-F46800?style=for-the-badge&logo=grafana&logoColor=white)

**AI / External API**

![Gmail API](https://img.shields.io/badge/Gmail%20API-EA4335?style=for-the-badge&logo=gmail&logoColor=white)
![Google PubSub](https://img.shields.io/badge/Google%20Pub%2FSub-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![FCM](https://img.shields.io/badge/FCM-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Portone](https://img.shields.io/badge/Portone-00B3E3?style=for-the-badge&logo=iota&logoColor=white)
![RAG](https://img.shields.io/badge/RAG%20AI%20Draft-8A2BE2?style=for-the-badge&logo=openai&logoColor=white)

</div>

---

## 📊 운영 성과

<div align="center">

| 구분 | 성과 |
|:---:|:---|
| 🧑‍💻 사용자 지표 | 실제 서비스 운영을 통해 MAU 200명 이상 확보 |
| 🧪 테스트 품질 | JUnit5 기반 Service Layer 테스트를 작성하여 테스트 커버리지 52% 달성 |
| 🔒 테스트 케이스 | 핵심 비즈니스 로직에 대해 80개 이상 Unit / 통합 테스트 작성 |
| 📈 UX 분석 | Amplitude Session Replay와 히트맵 분석을 활용해 계정 연동 및 라벨 관리 플로우 개선 |
| 🚨 장애 대응 | RabbitMQ DLQ와 Dead Letter Alert를 통해 실패 메시지 추적 및 이상 상황 탐지 |
| ⚙️ 처리 안정성 | Pub/Sub 수신 이후 메일 저장·분류·알림 작업을 비동기화하여 Backpressure 기반 처리 구조 |

</div>

---

## 🌱 팀 소개

<div align="center">

| 이름 | 학과 | 이메일 | 역할 |
|:---:|:---:|:---:|:---:|
| 김휘래 ([@rlagnlfo1004](https://github.com/rlagnlfo1004)) | 소프트웨어학과 | hrkim2001@ajou.ac.kr | **팀장** / 백엔드 개발 |
| 천진강 ([@jjjjjk12](https://github.com/jjjjjk12)) | 소프트웨어학과 | jjjjjk12@ajou.ac.kr | 인프라 / 백엔드 개발 |
| 곽민서 ([@mkms8436](https://github.com/mkms8436)) | 소프트웨어학과 | mkms0222@ajou.ac.kr | 디자인 / 프론트엔드 개발 |
| 한동현 ([@asitisdev](https://github.com/asitisdev)) | 소프트웨어학과 | hando1220@ajou.ac.kr | 인프라 / 프론트엔드 개발 |

</div>

---

<div align="center">

**아주대학교 소프트웨어학과 &nbsp;·&nbsp; 2026-1 SW캡스톤디자인 2조**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mailsangja)
&nbsp;
[![Service](https://img.shields.io/badge/Service-mail.ajou.app-4A90E2?style=for-the-badge&logo=googlechrome&logoColor=white)](https://mail.ajou.app/)
&nbsp;
[![SOFTCON](https://img.shields.io/badge/SOFTCON-2026--1-0057A8?style=for-the-badge&logo=academia&logoColor=white)](https://softcon.ajou.ac.kr/works/works.asp?uid=2298)

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer" />

</div>
