<br>
<div align="center">
  <img src="https://github.com/user-attachments/assets/e5b5f96c-9f57-458c-8137-d966bc7c23f3" width="197" />

  <h3 align="center">MaidRang</h3>

  <p align="center">
    메이드카페 출근표 · 이벤트 · 메이드 정보를 한 곳에서 확인하는 웹 플랫폼<br>
    <a href="https://maidrang.site"><strong>Web Service »</strong></a><br>
    <a href="https://github.com/MaidRang"><strong>Organization »</strong></a>
  </p>
</div>
<br>

<details open>
  <summary><strong>&nbsp;📖&nbsp;목차</strong></summary>

1. &nbsp;&nbsp;[🔍 Introduction](#-introduction)
2. &nbsp;&nbsp;[📄 Documents](#-documents)
3. &nbsp;&nbsp;[📹 Demo](#-demo)
4. &nbsp;&nbsp;[💡 Tech Stack](#-tech-stack)
5. &nbsp;&nbsp;[🗂️ Database](#%EF%B8%8F-database)
6. &nbsp;&nbsp;[💻 Architecture](#-architecture)
   - &nbsp;[System](#system)
   - &nbsp;[Auth](#auth)
7. &nbsp;&nbsp;[👨‍💻 Team](#-team)

</details>

<br>

## 🔍 Introduction

### 배경

메이드카페의 출근 정보와 이벤트 공지는 SNS, 이미지 공지, 개별 예약 페이지 등 여러 채널에 흩어져 있습니다.<br>
사용자는 **오늘 누가 출근하는지**, **어떤 이벤트가 진행 중인지**, **관심 있는 메이드의 다음 출근일이 언제인지**를 확인하기 위해 여러 채널을 반복해서 찾아야 합니다.

MaidRang은 이렇게 분산된 정보를 한 곳에서 확인할 수 있도록 만든 **메이드카페 정보 통합 플랫폼**입니다.<br>
카페별 메이드 프로필과 출근 일정, 이벤트 정보를 제공하고 즐겨찾기를 통해 관심 있는 메이드의 일정을 더 빠르게 확인할 수 있도록 구성했습니다.

### 특징

- **카페별 메이드 조회**&nbsp;:&nbsp;&nbsp;카페에 소속된 메이드 목록과 프로필 정보를 한 곳에서 조회
- **월별 출근표**&nbsp;:&nbsp;&nbsp;메이드별 근무 일정을 월 단위 캘린더 형태로 확인
- **관심 메이드 즐겨찾기**&nbsp;:&nbsp;&nbsp;자주 확인하는 메이드를 저장하고 관심 일정에 빠르게 접근
- **이벤트 확인**&nbsp;:&nbsp;&nbsp;카페별 이벤트 및 관련 이미지를 사용자에게 제공
- **소셜 로그인**&nbsp;:&nbsp;&nbsp;카카오 · 네이버 OAuth2 기반 로그인 지원
- **관리자 운영 기능**&nbsp;:&nbsp;&nbsp;메이드 정보 · 출근 일정 · 이벤트 등록/수정/삭제 관리
- **반응형 웹 서비스**&nbsp;:&nbsp;&nbsp;React 기반 웹 환경에서 카페 정보와 일정을 직관적으로 탐색

<br>

## 📄 Documents

- <strong>운영</strong>&nbsp;:&nbsp;&nbsp;2026 ~ end
  - Web&nbsp;:&nbsp;&nbsp;<a href="https://maidrang.site">maidrang.site</a>

- <strong>Backend API</strong>&nbsp;:&nbsp;&nbsp;Swagger 기반 API 문서화

- <strong>Deployment</strong>&nbsp;:&nbsp;&nbsp;AWS EC2 · RDS · Nginx · GitHub Actions

- <strong>주요 구현</strong>
  - Spring Security + JWT 기반 인증/인가
  - 카카오 · 네이버 OAuth2 로그인
  - 메이드 출근표 월별 조회 API
  - 사용자별 관심 메이드 즐겨찾기 및 일정 조회
  - 메이드 · 카페 · 출근 일정 · 이벤트 도메인 설계
  - React ↔ Spring Boot REST API 연동
  - GitHub Actions 기반 배포 자동화

<br>

## 📹 Demo

### Web Service

<div align="center">
  <a href="https://maidrang.site"><strong>🌐 MaidRang 서비스 바로가기</strong></a>
</div>

<!--
서비스 화면 캡처 업로드 후 아래 예시처럼 추가할 수 있습니다.

### Main Page

| 홈 | 카페 상세 | 출근표 |
| :---: | :---: | :---: |
| <img src="이미지_URL" width="100%"> | <img src="이미지_URL" width="100%"> | <img src="이미지_URL" width="100%"> |

### User Flow

| 로그인 | 메이드 목록 | 즐겨찾기 |
| :---: | :---: | :---: |
| <img src="이미지_URL" width="100%"> | <img src="이미지_URL" width="100%"> | <img src="이미지_URL" width="100%"> |
-->

<br>

## 💡 Tech Stack

|Frontend|Backend|Database|Security|Infra / DevOps|
|:------:|:------:|:------:|:------:|:------:|
|<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=white"/><br><img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/><br><img src="https://img.shields.io/badge/Emotion-C865B9?style=flat-square&logoColor=white"/><br><img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white"/>|<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/><br><img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/><br><img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/>|<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/><br><img src="https://img.shields.io/badge/AWS_RDS-527FFF?style=flat-square&logo=amazonrds&logoColor=white"/>|<img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/><br><img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white"/><br><img src="https://img.shields.io/badge/OAuth2-4285F4?style=flat-square&logoColor=white"/>|<img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white"/><br><img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/><br><img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>|

```text
- Frontend : React, TypeScript, Emotion, TanStack Query
- Backend : Spring Boot, Java, JPA
- Security : Spring Security, JWT, OAuth2 (Kakao · Naver)
- Database : MySQL, AWS RDS
- Deployment : AWS EC2, Nginx, GitHub Actions
- Tool : GitHub, Postman, Swagger
```

<br>

## 🗂️ Database

<details open>
  <summary>&nbsp;<strong>MySQL</strong>&nbsp;:&nbsp;&nbsp;<strong>서비스 핵심 데이터</strong></summary>

<br>

| 테이블 | 역할 |
| --- | --- |
| `USER` | 사용자 계정 및 인증 관련 정보 |
| `MAID_CAFE` | 메이드카페 기본 정보 |
| `MAID` | 카페별 메이드 프로필 정보 |
| `WORK_SCHEDULE` | 메이드별 출근 일정 |
| `FAVORITE` | 사용자 ↔ 관심 메이드 관계 |
| `CAFE_EVENT` | 카페별 이벤트 정보 |
| `EVENT_IMAGE` | 이벤트에 연결된 이미지 정보 |

</details>

<br>

## 💻 Architecture

### System
<img src="https://github.com/user-attachments/assets/6f6550c7-655c-48e5-9fa3-2918a2e33b27" width="100%" />

```text
- Client : React, TypeScript
- API Server : Spring Boot
- Authentication : Spring Security, JWT, OAuth2
- Database : AWS RDS (MySQL)
- Web Server / Reverse Proxy : Nginx
- Deployment : AWS EC2, GitHub Actions
```

<br>

## 👨‍👩‍👧‍👧 Team (Full Stack)

|                                              [박정우](https://github.com/jwoo13)                                              |
| :------------------------------------------------------------------------------------------------------------------------------: |
| <img width="300" src="https://github.com/user-attachments/assets/5dd961a4-062d-4725-bdb7-86b7c563bec2"> |
|                                                   Backend & Frontend Developer                                                    |
