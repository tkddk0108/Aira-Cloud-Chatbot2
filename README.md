# ☁️ Aira-2: 자동 오류 감지와 트랜잭션 무결성 강화

> 기간: 2025.01.16 ~ 2025.02.19  
> Aira 기능 고도화 및 클라우드 운영 안정성 향상을 위한 **ECS 기반 무중단 메시지 아키텍처 구현 프로젝트**

<img width="6210" height="4743" alt="image" src="https://github.com/user-attachments/assets/a4552532-7cde-4490-bdc4-1ff4b10010b0" />

---

## 🔧 프로젝트 개요

Aira-2는 OpenAI 기반 챗봇 Aira의 기능을 고도화하고 **클라우드 운영 안정성** 및 **트랜잭션 무결성** 확보를 위해 다음과 같은 목표로 수행된 프로젝트입니다.

- **목표**
  - EC2에서 **ECS Fargate 기반 서버리스** 전환
  - **트랜잭션 무결성**을 위한 **SQS + DLQ 구조**
  - **CI/CD 자동화**, 실시간 **오류 탐지 및 알림**, **2,000명 트래픽 대응 테스트**

---

## 🛠️ 주요 기술 스택 및 도구

| 항목 | 사용 기술 |
|------|-----------|
| 인프라 전환 | AWS ECS Fargate, ALB, VPC Endpoint |
| 메시지 처리 | SQS, Dead Letter Queue (DLQ) |
| CI/CD | GitHub Actions, ESLint, flake8 |
| 프론트엔드 | 인증/데이터 수집 화면 및 API 연동 |
| 모니터링 | Prometheus, Grafana, CloudWatch, AlertManager |
| 도메인/보안 | Route 53, HTTPS 인증서 (SSL) |
| 테스트 | Locust 기반 스트레스 테스트 (최대 2,000명) |

---

## 🗂️ 아키텍처 구성 요약

- **ECS Fargate 기반 무중단 배포 환경 구축**
  - EC2 → Fargate 전환으로 서버 운영 부담 제거
- **ALB + VPC Endpoint 도입**
  - 공용 인터넷 노출 최소화 및 보안 강화
- **SQS + DLQ 메시지 큐 구성**
  - GPT API 요청/응답을 비동기 처리하여 **트랜잭션 무결성 확보**
- **CI/CD 자동화**
  - GitHub Actions 기반 자동 빌드/배포 및 오류 알림
- **실시간 모니터링**
  - Prometheus + Grafana 대시보드 구성
  - AlertManager로 알림 시스템 완성
- **부하 테스트**
  - Locust로 최대 **2,000명 동시 접속 시나리오** 설계 및 검증

---

## ✅ 성과

- **트랜잭션 무결성 보장**: 메시지 유실 없는 비동기 구조 확보
- **2,000명 트래픽 대응 성공**: 스트레스 테스트에서 안정성 입증
- **운영 효율화**: 서버리스 전환으로 유지보수/관리 비용 감소
- **CI/CD 자동화**: 린트·배포 오류 탐지까지 포함된 DevOps 체계 완성

---

## 📂 주요 역할 및 기여

| 구분 | 상세 내용 |
|------|-----------|
| 프론트엔드 개발 | 사용자 인증, 데이터 수집 화면 구현 및 API 연동 |
| CI 파이프라인 | GitHub Actions 자동 빌드/배포, flake8 및 ESLint 검사 적용 |
| 메시지 처리 | GPT API 요청/응답 비동기 처리 및 DLQ 구성 |
| 도메인 설정 | Route53 HTTPS 인증서 설정 및 DNS 연결 |
| 부하 테스트 | Locust 기반 시나리오 설계 및 테스트 분석 |
| 문서화 및 발표 자료 | 전체 흐름 문서화, 발표용 PPT 및 최종 보고서 작성 주도 |

---

## 🔗 관련 링크

- [📎 발표 자료 (Google Drive)](https://drive.google.com/file/d/1tdnjwqJa6Cgkd09TVs68vAq_dWcBPvYK/view?usp=drive_link)

---

## 📌 향후 개선 방향

- AWS Lambda 기반 서버리스 API로 전환 검토
- API Gateway + WAF를 통한 보안 강화
- SQS 메시지 시각화 및 모니터링 자동화

---

> Aira-2는 클라우드 인프라 운영의 안정성과 트래픽 탄력성을 높이기 위한 실전 프로젝트로, MSA 구조 설계 및 DevOps 자동화 역량을 실무 수준으로 끌어올린 경험입니다.
